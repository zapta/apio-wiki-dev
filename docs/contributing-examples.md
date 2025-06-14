![](assets/apio-banner.svg)

# Contributing Apio examples

Apio's examples are stored in the `examples` directory of the [FPGAwars/apio-examples](https://github.com/FPGAwars/apio-examples) repository and are delivered in the Apio's `examples` package (type `apio examples list` to see it's version).

To contribute a new example send a pull-request to the [FPGAwars/apio-examples](https://github.com/FPGAwars/apio-examples) repository after confirming that it complies with the following requirements.

1. The example contains an `info` file with a single text line no longer than 50 chars that describes the example.
2. The example lints with no warnings and can be built and uploaded.
3. The example path is `examples/<board-id>/<example-name>` where `board-id` matches the board id in `apio.ini` and `example-name` contains only the char `a-z`, `0-9`, and `-` and starts with a letter.
4. The example contains at least one testbench that passes `apio test` and `apio sim` with no errors.
5. Each testbench has a matching '.gtkw' file with a GTKWave saved state. 

NOTES:
1. The example may have all the files in a single directory or they can be spread in sub directories.
2. The example may have any mix of Verilog `.v` files and System Verilog `.sv` files.
3. If `apio.ini` contains more than one env, the rules above apply to all the envs (when selected using the `--env env` flag).

<br>

![](assets/fpgawars-banner.svg)
