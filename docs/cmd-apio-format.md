

# Apio format

The command `apio format` formats the project's source files to ensure
consistency and style without altering their semantics. The command
accepts the names of specific source files to format or formats all
project source files by default.

#### EXAMPLES
```
apio format                    # Format all source files.
apio format -v                 # Same but with verbose output.
apio format main.v main_tb.v   # Format the two files.
```

#### OPTIONS
```
-e, --env name          Set the apio.ini env.
-p, --project-dir path  Set the root directory for the project.
-v, --verbose           Show detailed output.
-h, --help              Show this message and exit.
```

> The file arguments are relative to the project directory, even if the --project-dir option is used.

#### CUSROMIZATION

The format command utilizes the format tool from the Verible project,
which can be configured by setting its flags in the apio.ini project
file For example:

```
format-verible-options =
    --column_limit=80
    --indentation_spaces=4
```

#### CONTROL

If needed, sections of source code can be protected from formatting using Verible formatter directives:

```
// verilog_format: off
... untouched code ...
// verilog_format: on
```

For a full list of Verible formatter flags, refer to the documentation
page online or use the command `apio raw -- verible-verilog-format --helpful`.


<br>

