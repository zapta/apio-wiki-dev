# Apio info

The `apio info` command group provides additional information about Apio and your system.

## OPTIONS

`  -h, --help  Show this message and exit.`

## SUBCOMMANDS

```
  apio info platforms
  apio info system
  apio info colors
```

---

# Apio info platforms

The command `apio info platforms` lists the platform IDs supported by
Apio, with the effective platform ID of your system highlighted.

> [Advanced] The automatic platform ID detection of Apio can be overridden by
> defining a different platform ID using the `APIO_PLATFORM` environment
> variable. This is generally not recommended.

## EXAMPLES

```
apio info platforms   # List supported platform IDs.
```

## OPTIONS

```
-h, --help  Show this message and exit.
```

---

# Apio info system

The `apio info system` command displays general information about your
system and Apio installation. This is useful for diagnosing setup issues.

> [Advanced] The default location of the Apio home directory, where apio
> saves preferences and packages, is in the `.apio` directory under the
> user home directory but can be changed using the `APIO_HOME` environment variable.

## EXAMPLES

```
apio info system   # Show system information.
```

## OPTIONS

```
-h, --help  Show this message and exit.
```

---

# Apio info colors

The command `apio info colors` shows how ANSI colors are rendered on your platform, typically for diagnosing color-related issues. While the color name and styling is always handled by the Python Rich library, the output is shown using one of three libraries: Rich, Click, or Python's `print()`.

## EXAMPLES

```
apio info colors          # Rich library output (default)
apio info colors --rich   # Rich library output (same as above).
apio info colors --click  # Click library output.
apio info colors --print  # Python's print() output.
apio sys col -p           # Using shortcut.
```

## OPTIONS

```
-r, --rich   Output using the Rich library.
-c, --click  Output using the Click library.
-p, --print  Output using Python's print().
-h, --help   Show this message and exit.
```
