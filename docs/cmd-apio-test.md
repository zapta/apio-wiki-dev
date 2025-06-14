![](assets/apio-banner.svg)

# Apio test

  The command `apio test` simulates one or all the testbenches in the
  project and is useful for automated testing of your design.
  Testbenches are expected to have names ending with `_tb` (e.g.,
  `my_module_tb.v`) and should exit with the `$fatal` directive if an
  error is detected.

#### EXAMPLES
```
apio test                 # Run all *_tb.v testbenches.
apio test my_module_tb.v  # Run a single testbench.
```
#### OPTIONS
```
-e, --env name          Set the apio.ini env.
-p, --project-dir path  Set the root directory for the project.
-h, --help              Show this message and exit.
```

#### NOTES

* Do not use the Verilog `$dumpfile()` function in your
testbenches, as this may override the default name and location Apio
sets for the generated .vcd file.

* Testbench specification is always the testbench file path
relative to the project directory, even if using the `--project-dir`
option.

* For a sample testbench compatible with Apio features, the apio example `alhambra-ii/getting-started`.

* To simulate a testbench with a graphical visualization of the
  signals, refer to the `apio sim` command.

<br>

![](assets/fpgawars-banner.svg)