

```markdown
Register 5.21. IO_MUX_GPIOn_REG (n: 0-21) (0x0004+4*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                      |                                                                             |
| 16  | IO_MUX_GPIOn_FILTER_EN        |                                                                             |
| 15  | IO_MUX_GPIOn_MCU_SEL          |                                                                             |
| 14  | IO_MUX_GPIOn_FUN_DRV          |                                                                             |
| 12  | IO_MUX_GPIOn_WPU              |                                                                             |
| 11  | IO_MUX_GPIOn_WPD              |                                                                             |
| 10  | IO_MUX_GPIOn_MCU_IE           |                                                                             |
| 9   | IO_MUX_GPIOn_SLP_SEL          |                                                                             |
| 8   | IO_MUX_GPIOn_FUN_IE           |                                                                             |
| 7   | IO_MUX_GPIOn_MCU_OE            |                                                                             |
| 6   | IO_MUX_GPIOn_WPU              |                                                                             |
| 5   | IO_MUX_GPIOn_WPD              |                                                                             |
| 4   | IO_MUX_GPIOn_MCU_IE           |                                                                             |
| 3   | IO_MUX_GPIOn_SLP_SEL          |                                                                             |
| 2   | IO_MUX_GPIOn_FUN_IE           |                                                                             |
| 1   | IO_MUX_GPIOn_MCU_OE            |                                                                             |
| 0   | Reset                         | 0x0 Ox2 1 1 0 0 0 0 0 0 0 0 0 |

IO_MUX_GPIOn_MCU_OE Output enable of the pin in sleep mode. 1: output enabled; 0: output disabled. (R/W)

IO_MUX_GPIOn_SLP_SEL Sleep mode selection of this pin. Set to 1 to put the pin in sleep mode. (R/W)

IO_MUX_GPIOn_MCU_WPD Pull-down enable of the pin in sleep mode. 1: internal pull-down enabled; 0: internal pull-down disabled. (R/W)

IO_MUX_GPIOn_MCU_WPU Pull-up enable of the pin during sleep mode. 1: internal pull-up enabled; 0: internal pull-up disabled. (R/W)

IO_MUX_GPIOn_MCU_IE Input enable of the pin during sleep mode. 1: input enabled; 0: input disabled. (R/W)

IO_MUX_GPIOn_MCU_DRV Configures the drive strength of GPIOn during sleep mode.

- GPIO2, GPIO3, GPIO5, GPIO18, GPIO18, GPIO19
    - 0: ~5 mA
    - 1: ~20 mA
    - 2: ~10 mA
    - 3: ~40 mA

- Other GPIOs
    - 0: ~5 mA
    - 1: ~10 mA
    - 2: ~20 mA
    - 3: ~40 mA

(R/W)

IO_MUX_GPIOn_FUN_WPD Pull-down enable of the pin. 1: internal pull-down enabled; 0: internal pull-down disabled. (R/W)

IO_MUX_GPIOn_FUN_WPU Pull-up enable of the pin. 1: internal pull-up enabled; 0: internal pull-up disabled. (R/W)

IO_MUX_GPIOn_FUN_IE Input enable of the pin. 1: input enabled; 0: input disabled. (R/W)

Continued on the next page...
```