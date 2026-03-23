

```markdown
| Pin No.| Pin Name      | Function 0 | Function 1 | Function 2 | Function 3 | DRV | Reset | Notes |
|--------:|---------------|------------|------------|------------|------------|-----:|-------|-------|
|        4 | XTAL_32K_P    | GPIOO     | GPIOO      | -          | -          |   2 |   O   | R     |
|        5 | XTAL_32K_N    | GPIO1     | GPIO1      | -          | -          |   2 |   O   | R     |
|        6 | GPIO2         | GPIO2     | GPIO2      | FSPIQ      | -          |   2 |   1   | R     |
|        8 | GPIO3         | GPIO3     | GPIO3      | -          | -          |   2 |   1   | R     |
|        9 | MTMS          | MTMS      | GPIO4      | FSPIHD     | -          |   2 |   1   | R     |
|       10 | MTDI          | MTDI      | GPIO5      | FSPIWP     | -          |   2 |   1   | R     |
|       12 | MTCK          | MTCK      | GPIO6      | FSPICLK    | -          |   2 | 1*    | G     |
|       13 | MTDO          | MTDO      | GPIO7      | FSPID      | -          |   2 |   1   | G     |
|       14 | GPIO8         | GPIO8     | GPIO8      | -          | -          |   2 |   1   | -     |
|       15 | GPIO9         | GPIO9     | GPIO9      | -          | -          |   2 |   3   | -     |
|       16 | GPIO10        | GPIO10    | GPIO10     | FSPICS0    | -          |   2 |   1   | G     |
|       18 | VDD_SPI       | GPIO11    | GPIO11     | -          | -          |   2 |   O   | -     |
|       19 | SPIHD         | SPIHD     | GPIO12     | -          | -          |   2 |   3   | -     |
|       20 | SPIWP         | SPIWP     | GPIO13     | -          | -          |   2 |   3   | -     |
|       21 | SPICSO        | SPICSO    | GPIO14     | -          | -          |   2 |   3   | -     |
|       22 | SPICLK        | SPICLK    | GPIO15     | -          | -          |   2 |   3   | -     |
|       23 | SPID          | SPID      | GPIO16     | -          | -          |   2 |   3   | -     |
|       24 | SPIQ          | SPIQ      | GPIO17     | -          | -          |   2 |   3   | -     |
|       25 | GPIO18        | GPIO18    | GPIO18     | -          | -          |   3 |   O   | USB, G|
|       26 | GPIO19        | GPIO19    | GPIO19     | -          | -          |   3 | 0*    | USB   |
|       27 | UORXD         | UORXD     | GPIO20     | -          | -          |   2 |   3   | G     |
|       28 | UOTXD         | UOTXD     | GPIO21     | -          | -          |   2 |   4   | -     |

Drive Strength

“DRV” column shows the drive strength of each pin after reset:

• GPIO2, GPIO3, GPIO4, GPIO5, GPIO18, GPIO19
    – 0 - Drive current = ~5 mA
    – 1 - Drive current = ~20 mA
    – 2 - Drive current = ~10 mA
    – 3 - Drive current = ~40 mA

• Other GPIOs
    – 0 - Drive current = ~5 mA
    – 1 - Drive current = ~10 mA
```