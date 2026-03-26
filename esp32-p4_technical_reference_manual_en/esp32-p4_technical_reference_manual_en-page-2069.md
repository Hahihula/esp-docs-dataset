

```markdown
The test code loads when `CSI_HOST_PHY_TESTEN` is set to 1 and with the falling edge on `CSI_HOST_PHY_TESTCLK`.

- Ensure that `CSI_HOST_PHY_TESTCLK` is set to 1.
- Set `CSI_HOST_PHY_TESTDIN` to the 8-bit test code.
- Set `CSI_HOST_PHY_TESTEN` to 1.
- Set `CSI_HOST_PHY_TESTCLK` to 0. The falling edge on `CSI_HOST_PHY_TESTCLK` latches the value of `CSI_HOST_PHY_TESTDIN[7:0]` as the current test code.
- Set `CSI_HOST_PHY_TESTEN` to 0.

• Enter the test data.

The test data programs to the latest loaded test code when `CSI_HOST_PHY_TESTEN` is 0 and with the rising edge on `CSI_HOST_PHY_TESTCLK`.

- Set `CSI_HOST_PHY_TESTCLK` to 0, if not done already.
- Set `CSI_HOST_PHY_TESTDIN` to the 8-bit test data.
- Set `CSI_HOST_PHY_TESTCLK` to 1. The rising edge on `CSI_HOST_PHY_TESTCLK` programs the test data internally.

• Repeat the above steps to add more test data for the same test code.

Set `CSI_HOST_PHY_TESTCLR` to 1 to reset a test code. This is necessary only before the first programming operation or if you wish to reset the PHY’s configuration to its default value.

Figure 40.5-5 shows a timing diagram for the MIPI RX D-PHY control interface. After programming a test code, `CSI_HOST_PHY_TESTDOUT` asynchronously outputs the relevant data associated with the specific test code. This data may include read-back information or other meaningful signals.

![Figure 40.5-5. Control Interface Timing Diagram](image)

**Note:**

Some test codes require two write data operations. In the first operation, the value of `CSI_HOST_PHY_TESTCLK` changes from 1 to 0. Ensure that the falling edge in the clock does not occur when `CSI_HOST_PHY_TESTEN` is set to 1. Otherwise, the current test data will be latched as an erroneous test code.

It is highly recommended to set the test interface to an inactive state by programming the test code `0x00` when not
```