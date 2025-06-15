# Apio format

The `apio format` command formats the project's source files to ensure
consistent style without changing their semantics. It can format specific
files or all project source files by default.

> The file arguments are relative to the project directory, even if the `--project-dir` option is used.

## EXAMPLES

```
apio format                    # Format all source files.
apio format -v                 # Format all files with verbose output.
apio format main.v main_tb.v   # Format the two files.
```

## OPTIONS

```
-e, --env name          Use a named environment from apio.ini
-p, --project-dir path  Specify the project root directory
-v, --verbose           Show detailed output
-h, --help              Show this help message and exit
```

## CUSTOMIZATION

The format command utilizes the format tool from the Verible project,
which can be configured by adding a `format-verible-options` option in the project file `apio.ini`. For example:

```
format-verible-options =
    --column_limit=80
    --indentation_spaces=4
```

## PROTECTING CODE

Sections of source code can be protected from formatting using the Verible formatter directives:

```
// verilog_format: off
... untouched code ...
// verilog_format: on
```

For a full list of Verible formatter flags, refer to the documentation
page online or use the command `apio raw -- verible-verilog-format --helpful`.
