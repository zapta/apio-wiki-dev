# Apio fpgas

The `apio fpgas` command lists the FPGAs that are supported by Apio. You can define
custom FPGAs by placing a `fpgas.jsonc` file in the project directory,
which overrides the default one, as long as they are supported by the underlying tools..

## EXAMPLES

```
apio fpgas               # List all FPGAs.
apio fpgas -v            # List with extra columns.
apio fpgas | grep gowin  # Filter FPGA results.
```

## OPTIONS

```
-v, --verbose           Show detailed output
-p, --project-dir path  Specify the project root directory
-h, --help              Show this help message and exit
```
