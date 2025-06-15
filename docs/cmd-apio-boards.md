# Apio boards

The command `apio boards` lists the FPGA boards recognized by Apio.
Custom boards can be defined by placing a custom 'boards.jsonc' file
in the project directory, which will override Apio’s default
'boards.jsonc' file.

## EXAMPLES

```
apio boards                   # List all boards.
apio boards -v                # List with extra columns..
apio boards | grep ecp5       # Filter boards results.
```

## OPTIONS

```
-v, --verbose           Show detailed output.
-p, --project-dir path  Set the root directory for the project.
-h, --help              Show this message and exit.
```
