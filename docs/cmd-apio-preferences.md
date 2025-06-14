![](assets/apio-banner.svg)

# Apio preferences

The command `apio preferences` allows to view and manage the setting
of the apio's user's preferences. These settings are stored in the
`profile.json` file in the apio home directory (e.g. `~/.apio`) and
apply to all apio projects.

#### EXAMPLES
```
apio preferences -t light       # Colors for light backgrounds.
apio preferences -t dark        # Colors for dark backgrounds.
apio preferences -t no-colors   # No colors.
apio preferences --list         # List current preferences.
apio pref -t dark               # Using command shortcut.
```

#### OPTIONS
```
-t, --theme [light|dark|no-colors]  Set colors theme name.
-c, --colors                        List themes colors.
-l, --list                          List the preferences.
-h, --help                          Show this message and exit.
```

<br>

![](assets/fpgawars-banner.svg)