

# Apio command line

This page describes the principle and general options of using the Apio command line. For 
specific commands, see the respective command description.

----

### Apio command tree

Apio commands are organized as a tree of command that start with the 
root command `apio`. Some command such as `apio build` has only two 
levels of commands while others such `apio drivers install ftdi` have 
three or more. To explore the available commands at each
level, type the command with `-h` option (short for `--help`) to invoke its description. 

For example

```
  apio -h
  apio info -h
  apio info cli -h
```
-----

### Apio command options

Most of Apio's commands have options that allow to control their 
operation. For example, the command 'apio build' has options to 
control the verbosity of its output:

```
apio build --verbose
apio build --verbose-synth
```

For the list of options of each command type the command follows by a `-h` option (short for `--help`).
For example:

```
apio build -h
```
-----

### Apio command shortcuts

When typing apio commands, it's sufficient to type enough of each 
command to make the selection non ambiguous. For example, these commands
below are equivalent.

```
apio preferences
apio pref
apio pr
```
However, the command `apio p` is ambiguous because it matched both  
`apio preferences` and `apio packages`.

-----

### Apio shell auto completion

Apio's command line processor is based on the Python Click package 
which supports auto completion with some shells. While the were able 
to make it work as a proof of concept, this feature is experimental 
and is not guaranteed to work. More information is available in the 
Click's documentation at https://tinyurl.com/click-shell-completion.

-----
<br>

