
```markdown
| PMU_WAKEUP_ENA | Wake-up Sources       | Light-sleep | Deep-sleep |
|----------------|-----------------------|-------------|------------|
| 0x4            | GPIO¹                 | Y           | Y          |
| 0x8            | Wi-Fi beacon          | Y           | Y          |
| 0x10           | RTC Timer             | Y           | Y          |
| 0x20           | Wi-Fi²                | Y           | –          |
| 0x40           | UARTO³                | Y           | –          |
| 0x80           | UART1³                | Y           | –          |
| 0x100          | SDIO                  | Y           | –          |
| 0x400          | Bluetooth             | Y           | –          |
| 0x800          | LP CPU                | Y           | Y          |

```