![](assets/apio-banner.svg)

# Apio create

The command `apio create` creates a new `apio.ini` project file and is
typically used when setting up a new Apio project.

#### EXAMPLES
```
apio create --board alhambra-ii
apio create --board alhambra-ii --top-module MyModule
```

#### OPTIONS
```
-b, --board BOARD       Set the board.  [required]
-t, --top-module name   Set the top level module name.
-p, --project-dir path  Set the root directory for the project.
-h, --help              Show this message and exit.
```

#### NOTES
* This command only creates a new `apio.ini` file, rather than a
complete and buildable project. To create a complete project, use the 
`apio examples` command to fetch an example project for your board.

<br>

![](assets/fpgawars-banner.svg)