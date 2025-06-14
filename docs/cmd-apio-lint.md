![](assets/apio-banner.svg)

# Apio lint

The command `apio lint` scans the project's source files and reports errors, inconsistencies, and style violations. The command uses the `Verilator` tool, which is included with the standard Apio installation.

#### EXAMPLES
```
apio lint
apio lint -t my_module
apio lint --all
```

#### OPTIONS
```
--nostyle               Disable all style warnings.
--nowarn nowarn         Disable specific warning(s).
--warn warn             Enable specific warning(s).
-a, --all               Enable all warnings, including code style warnings.
-t, --top-module name   Restrict linting to this module and its
                          dependencies.
-e, --env name          Set the apio.ini env.
-p, --project-dir path  Set the root directory for the project.
-h, --help              Show this message and exit.
```

<br>

![](assets/fpgawars-banner.svg)