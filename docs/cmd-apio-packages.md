![](assets/apio-banner.svg)

# Apio packages

The command group `apio packages` provides commands to manage the
installation of Apio packages. These are not Python packages but Apio
packages containing various tools and data essential for the operation
of Apio.

The list of available packages depends on the operating system you are
using and may vary between different operating systems.

#### OPTIONS
```
-h, --help  Show this message and exit.
```

#### SUBCOMMANDS
```
apio packages update
apio packages list
```

<br>

-----

# Apio preferences update

The command `apio packages update` updates the installed Apio packages
to their latest requirements.

#### EXAMPLES
```
apio packages update            # Update packages
apio pack upd                   # Same, with shortcuts
apio packages update --force    # Force reinstallation from scratch
apio packages update --verbose  # Provide additional info
```

#### OPTIONS

```
-f, --force    Force reinstallation.
-v, --verbose  Show detailed output.
-h, --help     Show this message and exit.
```

#### NOTES

* Adding the `--force` option forces the reinstallation of existing
  packages; otherwise, packages that are already installed correctly
  remain unchanged.

* It is highly recommended to run the 'apio packages update' once in a
  while because it check the Apio remote server for the latest packages
  versions with potential fixes and additional examples.

<br>

-----

# Apio preferences list

The command `apio packages list` lists the available and installed
Apio packages. The list of available packages depends on the operating
system you are using and may vary between operating systems.

#### EXAMPLES
```
apio packages list
```

#### OPTIONS
```
-v, --verbose  Show detailed output.
-h, --help     Show this message and exit.
```


<br>

![](assets/fpgawars-banner.svg)