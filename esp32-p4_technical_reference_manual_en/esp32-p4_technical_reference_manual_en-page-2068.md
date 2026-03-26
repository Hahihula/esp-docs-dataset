

```markdown
STOP STATE LP-11
LP Receiver enabled

Escape mode sequence
LP-10, LP-00

ULPS LP-00
LP Receiver enabled

LP-10
LP receiver enabled

STOP STATE LP-11


Escape mode sequence
LP-10, LP-00, LP-01,
LP-00

ULPS command

ULPS LP-00
LP receiver enabled


Figure 40.5-4. ULPS Sequences for Clock and Data Lanes
```

## 40.5.3 MIPI RX D-PHY Configuration

The MIPI RX D-PHY includes test codes for configuring MIPI RX D-PHY operation. Refer to Section 40.5.3.2 for all supported test codes.

### 40.5.3.1 MIPI RX D-PHY Programming Interface

The MIPI RX D-PHY test code programming involves two steps: first, program the test code into the registers; second, provide the test data to the tester's inputs.

Before configuring a test code, perform the following steps:

*   Write 0 to `CSI_HOST_PHY_SHUTDOWNZ` and `CSI_HOST_DPHY_RSTZ` to shut down and reset the PHY.
*   It is also recommended to set `CSI_HOST_PHY_TESTCLR` to 1 to apply a reset pulse before the first configuration of any test code.

Next, configure the test code by following these steps:

*   Set the test code.
```