![](assets/apio-banner.svg)

# Apio Project Structure

## Directory structure

An Apio project is made of a directory that contains the required project file `apio.ini` and the project files. Below is an example of a minimal ICE40 project (`alhambra-ii/blinky` example) which contains the project file `apio.ini`, a Verilog source file `blinkey.v` and the pinout constraints file `pinout.pcf` which maps symbolic pin names to pin number.

```
my-project/
├── apio.ini
├── blinky.v
└── pinout.pcf
```

The next example (alhambra-ii/bcd-output) is more complex with the Verilog `*.v` source files, their `_tb.*` testbenches and their `*.gtkw` GTKWave states are organized in directory tree.

```
my-project/
├── apio.ini
├── bcd
│   ├── bcd_digit_tb.gtkw
│   ├── bcd_digit_tb.v
│   └── bcd_digit.v
├── main_tb.gtkw
├── main_tb.v
├── main.v
├── pinout.pcf
├── testing
│   └── apio_testing.vh
└── util
    ├── reset_gen.v
    ├── ticker_tb.gtkw
    ├── ticker_tb.v
    └── ticker.v
```

**Directory structure rules**
* The project file `apio.ini` and the pinout constraints file should reside in at the top directory.
* Source files and testbenches can reside in the root directory or in any sub directory. 
* Testbenches GTKWave state files (`.gtkw`) should reside in the directory of their respective testbenches.

## Output files

Apio commands write their output to the directory `_build/<env>` under the project root directory, where `<env>` is the active env name from apio.ini. For example, when building for an env called `default`, the output directory is `_build/default`. The example below shows the results of the `apio build` command with the ICE40 bitstream file `hardware.bin` and intermediate files that were created during the build.

```
my-project/
├── _build
│   └── default
│       ├── hardware.asc
│       ├── hardware.bin
│       ├── hardware.json
│       ├── hardware.pnr
│       └── scons.params
├── apio.ini
├── blinky.v
└── pinout.pcf
```

> The command `apio clean` can be used to delete all of Apio generated files and to force a build from scratch.

## Using Git

When working with git, we recommend to include the following in your `.gitignore` file.

**.gitignore**
```
_build
.DS_Store
```

<br>

![](assets/fpgawars-banner.svg)