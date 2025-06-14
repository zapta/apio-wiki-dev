![](assets/apio-banner.svg)

# Using testbenches

Testbenches are non synthesizable Verilog files with the suffix `_tb.v` and System Verilog files with the suffix `_tb.sv` that are used to simulate and test the synthesizable modules of the project. Testbenches are used by the command `apio sim` for simulation with a graphical view of the signals and by `apio test` for a bulk test that none of the assertions in the testbenches fails.

Testbenches files can be placed anywhere is the project directory tree, near the modules they tests, or in a separate directory that is dedicated for testing. When you run `apio sim` and view the results in GTKWave, it is recommended to save the GTKWave configuration in a `.gtkw` file with name of its testbench such that it will take affect next time you run `apio sim`.

Apio defines the Verilog macro when running `apio sim` and doesn't define it when running `apio test`. This allow to condition calls to $fail such that the simulation exists with an error when run in batch mode using `apio test` but it continues and emits the wave file when run using `apio sim`.

Make sure that your testbenches do not call `$fumpfile()` and to let Apio set the desire location for the generated signal files. Failing to do so may result in apio not be able to find the file when opening the GTKWave signal viewer or when cleaning the project.

## Instructions for AI
One way to write testbenches is to feed the tested module and instructions to an AI engine and ask it to generate the testbench code. The rules below can be copy/paste into the AI prompt to let it know of Apio's requirements.

> Apio testbench rules
> * Rule 1: Use $dumpvars() with the testbench module name as an argument.
> * Rule 2: Do not use $dumpfile().
> * Rule 3: Compare expected values to actual values and if they don't match, print an error message and call $fatal to exit.
> * Rule 4: Anytime you call $fatal in the testbench, first test the condition `ifndef INTERACTIVE_SIM, skip $fatal if the condition is false. 
> * Rule 5: At the end of the testbench print the message "End of simulation".
> * Rule 6: Create in the testbench a boolean signal called tb_error with the initial value of 0 and the comment "Set to high on first error" and set it to 1 each time an actual value doesn't match the expected value.

Example, giving this module text to ChatGPT, together with the rules
```
module Main #(
    parameter integer N = 3_000_000
) (
    input  CLK,        // 12MHz clock
    output [7:0] ROWS, // LED rows
    output [3:0] COLS  // LED columns
);

  reg [31:0] counter = 0;

  reg toggle = 0;

  // Rows and columns are active low.
  assign ROWS = {6'b111111, toggle, ~toggle};
  assign COLS = 4'b1110;

  always @(posedge CLK) begin
    if (counter >= N - 1) begin
      counter <= 0;
      toggle <= !toggle;
    end else begin
      counter <= counter + 1;
    end
  end

endmodule
```

The provided testbench.
```

```

<br>

![](assets/fpgawars-banner.svg)