

# Apio upload

The command `apio upload` builds the bitstream file (similar to the `apio build` command) and then uploads it to the FPGA board.

#### EXAMPLES
```
apio upload                            # Typical invocation
apio upload -s /dev/cu.usbserial-1300  # Select serial port
apio upload -n FTXYA34Z                # Select serial number
```

#### OPTIONS
```
-s, --serial-port serial-port  Set the serial port.
-n, --serial-num serial-num    Select the device's USB serial number.
-e, --env name                 Set the apio.ini env.
-p, --project-dir path         Set the root directory for the project.
-h, --help                     Show this message and exit.
```

Typically the simple form `apio upload` is sufficient to locate and program the FPGA board. The optional flags `--serial-port` and `--serial-num` allows to select the desired board if more than one matching board is found.

> You can use the command `apio devices` to list the connected USB and serial devices and the command `apio drivers` to install and uninstall device drivers.

> The default programmer command of your board can be overridden using the `apio.ini` option `programmer-cmd`.



<br>

