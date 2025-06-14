![](assets/apio-banner.svg)

# Apio graph

The command `apio graph` generates a graphical representation of the design.

#### EXAMPLES
```
apio graph               # Generate a svg file.
apio graph --svg         # Generate a svg file.
apio graph --pdf         # Generate a pdf file.
apio graph --png         # Generate a png file.
apio graph -t my_module  # Graph my_module module.
```
#### OPTIONS
```
--svg                   Generate a svg file (default).
--png                   Generate a png file.
--pdf                   Generate a pdf file.
-e, --env name          Set the apio.ini env.
-p, --project-dir path  Set the root directory for the project.
-t, --top-module name   Set the name of the top module to graph.
-v, --verbose           Show detailed output.
-h, --help              Show this message and exit.
```

#### NOTES

* On Windows, type `explorer _build/default/hardware.svg` to view
  the graph, and on Mac OS type `open _build/default/hardware.svg` (if
  your env is different than `default` change the commands accordingly).

<br>

Example `apio graph` generated graph:

![](assets/apio-graph.svg)

<br>

![](assets/fpgawars-banner.svg)