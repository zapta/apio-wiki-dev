![](assets/apio-banner.svg)

# FPGA Board Drivers

With some platforms and boards, it may be necessary to install a system driver to make the board accessible by the programmer. If this becomes necessary, use the `apio drivers install` command to install the necessary driver. 

Apio comes with two kinds of drivers called 'ftdi' and 'serial' and the table below summarized the differences between them.

> Drivers installation is not required of Mac OSX.

> If the FPGA board is shown in the device list with `--unavail--` manufactuer or product string, it's typically an indication that the proper driver need to be install. 


|   | FTDI drivers | Serial drivers   |
|--------|:-----|:------------|
| Platforms  | Linux, Windows  | Linux, Windows   |
| Driver install  | `apio drivers install ftdi`  | `apio drivers install serial`   |
| Driver uninstall  | `apio drivers uninstall ftdi`  | `apio drivers uninstall serial`   |
| List devices    | `apio devices usb`  | `apio devices serial`    |



<br>

![](assets/fpgawars-banner.svg)