

```markdown
| GPIO No. | Pin Name   | Function 0 | Function 1 | Function 2 | Function 3 | DRV | Reset | Notes |
|----------|------------|------------|------------|------------|------------|-----|-------|-------|
| 0        | XTAL_32K_P | GPIO0      | GPIO0      | —          | —          | 2   | 0     | R     |
| 1        | XTAL_32K_N | GPIO1      | GPIO1      | —          | —          | 2   | 0     | R     |
| 2        | GPIO2      | GPIO2      | GPIO2      | FSPIQ      | —          | 2   | 0     | R     |
| 3        | MTMS       | MTMS       | GPIO3      | FSPIHD     | —          | 2   | 1     | R     |
| 4        | MTDI       | MTDI       | GPIO4      | FSPIWP     | —          | 2   | 1     | R     |
| 5        | MTCK       | MTCK       | GPIO5      | —          | —          | 2   | 1*    | R     |
| 6        | MTDO       | MTDO       | GPIO6      | FSPICLK    | —          | 2   | 1     | R     |
| 7        | GPIO7      | GPIO7      | GPIO7      | FSPID      | —          | 2   | 1     | R     |
| 8        | GPIO8      | GPIO8      | GPIO8      | FSPICSO    | —          | 2   | 1     |       |
| 9        | GPIO9      | GPIO9      | GPIO9      | —          | —          | 2   | 3     | —     |
| 10       | UORXD      | UORXD      | GPIO10     | —          | —          | 2   | 1     | —     |
| 11       | UOTXD      | UOTXD      | GPIO11     | —          | —          | 2   | 4     | —     |
| 12       | GPIO12     | GPIO12     | GPIO12     | —          | —          | 3   | 1     | USB   |
| 13       | GPIO13     | GPIO13     | GPIO13     | —          | —          | 3   | 3*    | USB   |
| 22       | SDIO_DATA2 | SDIO_DATA2 | GPIO22     | —          | —          | 2   | 1     | —     |
| 23       | SDIO_DATA3 | SDIO_DATA3 | GPIO23     | —          | —          | 2   | 1     | —     |
| 24       | GPIO24     | GPIO24     | GPIO24     | —          | —          | 2   | 0     | —     |
| 25       | SDIO_CMD   | SDIO_CMD   | GPIO25     | —          | —          | 2   | 1     | —     |
| 26       | SDIO_CLK   | SDIO_CLK   | GPIO26     | —          | —          | 2   | 1     | —     |
| 27       | SDIO_DATA0 | SDIO_DATA0 | GPIO27     | —          | —          | 2   | 1     | —     |
| 28       | SDIO_DATA1 | SDIO_DATA1 | GPIO28     | —          | —          | 2   | 1     | —     |
| 29       | GPIO29     | GPIO29     | GPIO29     | —          | —          | 2   | 0     | —     |

Notice:
In HP IO MUX, unused pins must be configured to GPIO function.

Drive Strength
“DRV” column shows the drive strength of each pin after reset:
• 0 - Drive current = ~5 mA
• 1 - Drive current = ~10 mA
• 2 - Drive current = ~20 mA
• 3 - Drive current = ~40 mA

Reset
The default configuration of each pin after reset:
• 0 - IE = 0 (input disabled)
• 1 - IE = 1 (input enabled)
```