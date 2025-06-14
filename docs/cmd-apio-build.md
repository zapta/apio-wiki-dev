![](assets/apio-banner.svg)

# Apio build

The command `apio build` processes the project’s synthesis source
files and generates a bitstream file, which can then be uploaded to
your FPGA.

#### EXAMPLES
```
apio build                   # Typical usage
apio build -e debug          # Set the apio.ini env.
apio build -v                # Verbose info (all)
apio build --verbose-synth   # Verbose synthesis info
apio build --verbose-pnr     # Verbose place and route info
```


#### OPTIONS
```
-e, --env name          Set the apio.ini env.
-p, --project-dir path  Set the root directory for the project.
-v, --verbose           Show detailed output.
--verbose-synth         Show detailed synth stage output.
--verbose-pnr           Show detailed pnr stage output.
-h, --help              Show this message and exit.
```

#### NOTES

  * The top module should be specified using the `top-module` option in `apio.ini`. 
  * The files are sorted in a deterministic lexicographic order.
  * The build command ignores testbench files (`*_tb.v`, and `*_tb.sv`).
  * It is unnecessary to run `apio build` before `apio upload`.
  * To force a rebuild from scratch run `apio clean` first.


<br>

![](assets/fpgawars-banner.svg)