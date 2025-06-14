

# Apio report

The command `apio report` provides information on the utilization and
timing of the design. It is useful for analyzing utilization
bottlenecks and verifying that the design can operate at the desired
clock speed.

#### EXAMPLES
```
apio report            # Print report.
apio report --verbose  # Print extra information.
```

#### OPTIONS
```
-e, --env name          Set the apio.ini env.
-p, --project-dir path  Set the root directory for the project.
-v, --verbose           Show detailed output.
-h, --help              Show this message and exit.
```

Example report
```
FPGA Resource Utilization                       
┌────────────────┬────────┬──────────┬─────────┐
│  RESOURCE      │  USED  │   TOTAL  │  UTIL.  │
├────────────────┼────────┼──────────┼─────────┤
│  ICESTORM_LC   │    90  │    7680  │     1%  │
│  ICESTORM_PLL  │        │       2  │         │
│  ICESTORM_RAM  │        │      32  │         │
│  SB_GB         │     2  │       8  │    25%  │
│  SB_IO         │     9  │     256  │     3%  │
│  SB_WARMBOOT   │        │       1  │         │
└────────────────┴────────┴──────────┴─────────┘

Clock Information              
┌─────────┬───────────────────┐
│  CLOCK  │  MAX SPEED [Mhz]  │
├─────────┼───────────────────┤
│  CLK    │           119.15  │
└─────────┴───────────────────┘
```


