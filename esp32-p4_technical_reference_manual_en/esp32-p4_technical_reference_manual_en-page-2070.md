

```markdown
## 40.5.3.2 MIPI RX D-PHY Test Code

The MIPI RX D-PHY is configured through test codes via `CSI_HOST_PHY_TEST_CTRL0_REG` and `CSI_HOST_PHY_TEST_CTRL1_REG`. Refer to Section 40.5.3.1 MIPI RX D-PHY Programming Interface for more details.

### Normal Operation

Use the following test code to enable normal operation of the PHY and the wake-up state of the test interface. In this mode, the test interface is inactive.

- Test Code: `0x00`
- Test Data: None

#### HS RX Control of Lane 0

Use the following test code to select the HS operating frequency range (hsfregrange).

- Test Code: `0x44`
- Test Data:

Table 40.5-3. Test Data in HS RX Control of Lane 0

| w-1'b0 | w-6'b0 | w-1'b0 |
|--------|--------|--------|
| Program Selector | HS operating frequency range selection (hsfregrange) | Reserved |

When Program Selector is `0`, Test Data[6:1] programs hsfregrange.

- Test Dout:

Table 40.5-4. Test Dout in HS RX Control of Lane 0

| r-1'b0 | r-6'b0 | r-1'b0 |
|--------|--------|--------|
| 1'b0   | HS operating frequency range selection (hsfregrange) | 1'b0 |

When `CSI_HOST_PHY_TESTDIN[7]` is `0`, Test Dout[6:1] reflects the value of the programmed hsfregrange.

### Others

Other test codes are reserved.

## 40.5.4 Descrambler

Data scrambling uses randomization techniques to mitigate electromagnetic interference (EMI) and radio frequency (RF) self-interference. This spreads the transmission energy of the link across a wider frequency band.
```