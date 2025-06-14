![](assets/apio-banner.svg)

# Using Apio's examples

Apio comes with a set of sample projects that demonstrates its features and can be used as a starting point for your own projects. To list the available examples type

```
$ apio examples list

┌──────────────────────────────────────┬───────┬─────────────────────────────────────────────────────────────┐
│ BOARD/EXAMPLE                        │ ARCH  │ DESCRIPTION                                                 │
├──────────────────────────────────────┼───────┼─────────────────────────────────────────────────────────────┤
│ alchitry-cu/blinky                   │ ice40 │ Blinking all leds                                           │
│ alhambra-ii/bcd-counter              │ ice40 │ Verilog example with testbenches and subdirectories.        │
│ alhambra-ii/bcd-counter-sv           │ ice40 │ System Verilog example with testbenches and subdirectories. │
│ alhambra-ii/blinky                   │ ice40 │ Blinking led                                                │
│ alhambra-ii/getting-started          │ ice40 │ Example for Apio getting-Starting docs.                     │
│ alhambra-ii/ledon                    │ ice40 │ Turning on a led                                            │

(truncated)

│ sipeed-tang-nano-9k/blinky-sv        │ gowin │ Blinking led (system verilog)                               │
│ sipeed-tang-nano-9k/pll              │ gowin │ PLL clock multiplier                                        │
└──────────────────────────────────────┴───────┴─────────────────────────────────────────────────────────────┘
```

To fetch an example type

```
# Create an empty project dir
$ apio mkdir work
$ cd work

# Fetch the example
$ apio example fetch alhambra-ii/getting-started

# List the files
$ tree .
.
├── apio.ini
├── main_tb.gtkw
├── main_tb.v
├── main.v
└── pinout.pcf

# Show the project file.
$ cat -n apio.ini
     1	; Apio project file.
     2	
     3	[env:default]
     4	
     5	; Board id.
     6	board = alhambra-ii
     7	
     8	; Top module name (in main.v)
     9	top-module = Main

```

The fetched example is now an Apio project which can be build and uploaded to a matching FPGA board.

<br>

![](assets/fpgawars-banner.svg)