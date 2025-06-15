# Apio examples

The command group `apio examples` provides subcommands for listing and
fetching Apio provided examples. Each example is a self contained mini
project that can be built and uploaded to an FPGA board.

## EXAMPLES

```
-h, --help  Show this message and exit.
```

## SUBCOMMANDS

```
apio examples list
apio examples fetch
```

---

# Apio examples list

The command `apio examples list` lists the available Apio project
examples that you can use.

## EXAMPLES

```
apio examples list                     # List all examples
apio examples list  -v                 # More verbose output.
apio examples list | grep alhambra-ii  # Show alhambra-ii examples.
apio examples list | grep -i blink     # Show blinking examples.
```

## OPTIONS

```
-v, --verbose  Show detailed output.
-h, --help     Show this message and exit.
```

---

# Apio examples fetch

The command `apio examples fetch` fetches a single examples or all the
examples of a board. The destination directory is either the current
directory or the directory specified with `--dst` and it should be
empty and non existing.

## EXAMPLES

```
apio examples fetch alhambra-ii/ledon    # Single example
apio examples fetch alhambra-ii          # All board's examples
apio examples fetch alhambra-ii -d work  # Explicit destination
```

## OPTIONS

```
-d, --dst path  Set a different destination directory.
-h, --help      Show this message and exit.
```
