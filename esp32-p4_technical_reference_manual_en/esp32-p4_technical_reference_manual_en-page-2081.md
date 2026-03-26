

```markdown
Register 40.7. CSI_HOST_PHY_TEST_CTRL0_REG (0x0050)

| Bit | Field Name           | Description                                                                 |
|-----|----------------------|-----------------------------------------------------------------------------|
| 31  | reserved             |                                                                             |
| 2   | CSI_HOST_PHY_TESTCLR | Configures whether to initialize the test code interface.                    |
|     |                      | O: Not initialize                                                            |
|     |                      | 1: Initialize                                                                |
|     |                      | To ensure the analog programmability default values are preset, this bit must be set to 1 then clear to 0 after power-up. (R/W) |
| 1   | CSI_HOST_PHY_TESTCLK | Configures clock to capture CSI_HOST_PHY_TESTDIN bus contents into D-PHY test code logic, with CSI_HOST_PHY_TESTEN controlling the operation selection. (R/W) |

Register 40.8. CSI_HOST_PHY_TEST_CTRL1_REG (0x0054)

| Bit | Field Name           | Description                                                                 |
|-----|----------------------|-----------------------------------------------------------------------------|
| 31  | reserved             |                                                                             |
| 17  | CSI_HOST_PHY_TESTEN  | Configures the 8-bit data input of the test code interface for programming internal registers and accessing test functionalities. (R/W) |
| 16  |                      |                                                                             |
| 8   | CSI_HOST_PHY_TESTDOUT| Represents the 8-bit data output of the test code interface for reading data and other probing functionalities. (RO) |
| 7   |                      |                                                                             |
| 0   |                      |                                                                             |

CSI_HOST_PHY_TESTEN Configures whether to performs the test data write operation of the test code interface on the rising edge or the falling edge of CSI_HOST_PHY_TESTCLK.
O: On the rising edge
1: On the falling edge
(R/W)
```