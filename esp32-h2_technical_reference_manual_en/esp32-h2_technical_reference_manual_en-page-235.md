

# 6.13 IO MUX Functions List

Table 6.13-1 shows the IO MUX functions of each GPIO pin.

## Table 6.13-1. IO MUX Functions List

| GPIO | Pin Name   | Function 0 | Function 1 | Function 2 | Function 3 | DRV | Reset | Notes |
|------|------------|------------|------------|------------|------------|-----|-------|-------|
| 0    | GPIO0      | GPIO0      | GPIO0      | FSPIQ      | —          | 2   | 0     | —     |
| 1    | GPIO1      | GPIO1      | GPIO1      | FSPICSO    | —          | 2   | 0     | —     |
| 2    | MTMS       | MTMS       | GPIO2      | FSPIWP     | —          | 2   | 1     | —     |
| 3    | MTDO       | MTDO       | GPIO3      | FSPIHD     | —          | 2   | 1     | —     |
| 4    | MTCK       | MTCK       | GPIO4      | FSPICLK    | —          | 2   | 1*    | —     |
| 5    | MTDI       | MTDI       | GPIO5      | FSPID      | —          | 2   | 1     | —     |
| 8    | GPIO8      | GPIO8      | GPIO8      | —          | —          | 2   | 1     | R     |
| 9    | GPIO9      | GPIO9      | GPIO9      | —          | —          | 2   | 3     | R     |
| 10   | GPIO10     | GPIO10     | GPIO10     | —          | —          | 2   | 0     | R     |
| 11   | GPIO11     | GPIO11     | GPIO11     | —          | —          | 2   | 0     | R     |
| 12   | GPIO12     | GPIO12     | GPIO12     | —          | —          | 2   | 0     | R     |
| 13   | XTAL_32K_P | GPIO13     | GPIO13     | —          | —          | 2   | 0     | R     |
| 14   | XTAL_32K_N | GPIO14     | GPIO14     | —          | —          | 2   | 0     | R     |
| 22   | GPIO22     | GPIO22     | GPIO22     | —          | —          | 2   | 0     | —     |
| 23   | UORXD      | UORXD      | GPIO23     | FSPICS1    | —          | 2   | 3     | —     |
| 24   | UOTXD      | UOTXD      | GPIO24     | FSPICS2    | —          | 2   | 4     | —     |
| 25   | GPIO25     | GPIO25     | GPIO25     | FSPICS3    | —          | 2   | 1     | —     |
| 26   | GPIO26     | GPIO26     | GPIO26     | FSPICS4    | —          | 3   | 1     | USB   |
| 27   | GPIO27     | GPIO27     | GPIO27     | FSPICS5    | —          | 3   | 3*    | USB   |

## Drive Strength

“DRV” column shows the drive strength of each pin after reset:

- **0** - Drive current = ~5 mA
- **1** - Drive current = ~10 mA
- **2** - Drive current = ~20 mA
- **3** - Drive current = ~40 mA

## Reset Configurations

“Reset” column shows the default configuration of each pin after reset:

- **0** - IE = 0 (input disabled)
- **1** - IE = 1 (input enabled)
- **2** - IE = 1, WPD = 1 (input enabled, pull-down resistor enabled)
- **3** - IE = 1, WPU = 1 (input enabled, pull-up resistor enabled)
- **4** - OE = 1, WPU = 1 (output enabled, pull-up resistor enabled)