

# 7.12 IO MUX Functions List

Table 7.12-1 shows the IO MUX functions of each GPIO pin.

## Table 7.12-1. IO MUX Functions List

| GPIO | Pin Name     | Function 0 | Function 1 | Function 2 | Function 3 | DRV | Reset | Notes |
|------|--------------|------------|------------|------------|------------|-----|-------|-------|
| 0    | XTAL_32K_P   | GPIO0      | GPIO0      | —          | —          | 2   | 0     | R     |
| 1    | XTAL_32K_N   | GPIO1      | GPIO1      | —          | —          | 2   | 0     | R     |
| 2    | GPIO2        | GPIO2      | GPIO2      | FSPIQ      | —          | 2   | 1     | R     |
| 3    | GPIO3        | GPIO3      | GPIO3      | —          | —          | 2   | 1     | R     |
| 4    | MTMS         | MTMS       | GPIO4      | FSPIHD     | —          | 2   | 1     | R     |
| 5    | MTDI         | MTDI       | GPIO5      | FSPIWP     | —          | 2   | 1     | R     |
| 6    | MTCK         | MTCK       | GPIO6      | FSPICLK    | —          | 2   | 1*    | R     |
| 7    | MTDQ         | MTDQ       | GPIO7      | FSPID      | —          | 2   | 1     | R     |
| 8    | GPIO8        | GPIO8      | GPIO8      | —          | —          | 2   | 1     | —     |
| 9    | GPIO9        | GPIO9      | GPIO9      | —          | —          | 2   | 3     | —     |
| 10   | GPIO10       | GPIO10     | GPIO10     | —          | —          | 2   | 1     | S1    |
| 11   | GPIO11       | GPIO11     | GPIO11     | —          | —          | 2   | 1     | S1     |
| 12   | GPIO12       | GPIO12     | GPIO12     | —          | —          | 3   | 1     | USB    |
| 13   | GPIO13       | GPIO13     | GPIO13     | —          | —          | 3   | 3     | USB    |
| 14   | GPIO14       | GPIO14     | GPIO14     | —          | —          | 2   | 1     | S0     |
| 15   | GPIO15       | GPIO15     | GPIO15     | —          | —          | 2   | 1     | —      |
| 16   | UOTXD        | UOTXD      | GPIO16     | FSPICS0    | —          | 2   | 4     | —      |
| 17   | UORXD        | UORXD      | GPIO17     | FSPICS1    | —          | 2   | 3     | —      |
| 18   | SDIO_CMD     | SDIO_CMD   | GPIO18     | FSPICS2    | —          | 2   | 3     | —      |
| 19   | SDIO_CLK     | SDIO_CLK   | GPIO19     | FSPICS3    | —          | 2   | 3     | —      |
| 20   | SDIO_DATA0   | SDIO_DATA0 | GPIO20     | FSPICS4    | —          | 2   | 3     | —      |
| 21   | SDIO_DATA1   | SDIO_DATA1 | GPIO21     | FSPICS5    | —          | 2   | 3     | —      |
| 22   | SDIO_DATA2   | SDIO_DATA2 | GPIO22     | —          | —          | 2   | 3     | —      |
| 23   | SDIO_DATA3   | SDIO_DATA3 | GPIO23     | —          | —          | 2   | 3     | —      |
| 24   | SPICS0       | SPICS0     | GPIO24     | —          | —          | 2   | 3     | S1, S2 |
| 25   | SPIQ         | SPIQ       | GPIO25     | —          | —          | 2   | 3     | S1, S2 |
| 26   | SPIWP        | SPIWP      | GPIO26     | —          | —          | 2   | 3     | S1, S2 |
| 27   | VDD_SPI      | GPIO27     | GPIO27     | —          | —          | 2   | 0     | S1, S2 |
| 28   | SPIHD        | SPIHD      | GPIO28     | —          | —          | 2   | 3     | S1, S2 |
| 29   | SPICLK       | SPICLK     | GPIO29     | —          | —          | 2   | 3     | S1, S2 |
| 30   | SPID         | SPID       | GPIO30     | —          | —          | 2   | 3     | S1, S2 |

## Drive Strength

“DRV” column shows the drive strength of each pin after reset:

* `0` - Drive current = ~5 mA
* `1` - Drive current = ~10 mA
* `2` - Drive current = ~20 mA