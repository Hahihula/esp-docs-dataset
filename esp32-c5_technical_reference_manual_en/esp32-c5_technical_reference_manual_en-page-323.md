

```markdown
| GPIO No. | Name    | Function 0 | Function 1* | Function 2 | Function 3 | DRV | Reset | Notes |
|----------|---------|------------|-------------|------------|------------|-----|-------|-------|
| 9        | GPIO9   | SDIO_CLK   | GPIO9       | —          | —          | 2   | 0     | —     |
| 10       | GPIO10  | SDIO_CMD   | GPIO10      | FSPICSO    | —          | 2   | 0     | —     |
| 11       | UOTXD   | UOTXD      | GPIO11      | —          | —          | 2   | 4     | —     |
| 12       | UORXD   | UORXD      | GPIO12      | —          | —          | 2   | 1     | —     |
| 13       | GPIO13  | SDIO_DATA3 | GPIO13      | —          | —          | 3   | 1     | USB   |
| 14       | GPIO14  | SDIO_DATA2 | GPIO14      | —          | —          | 3   | 3*    | USB   |
| 23       | GPIO23  | GPIO23     | GPIO23      | —          | —          | 2   | 0     | —     |
| 24       | GPIO24  | GPIO24     | GPIO24      | —          | —          | 2   | 0     | —     |
| 25       | GPIO25  | GPIO25     | GPIO25      | —          | —          | 2   | 1     | —     |
| 26       | GPIO26  | GPIO26     | GPIO26      | —          | —          | 2   | 1     | —     |
| 27       | GPIO27  | GPIO27     | GPIO27      | —          | —          | 2   | 3     | —     |
| 28       | GPIO28  | GPIO28     | GPIO28      | —          | —          | 2   | 3     | —     |

* In HP IO MUX, unused pins must be configured to GPIO function.
```