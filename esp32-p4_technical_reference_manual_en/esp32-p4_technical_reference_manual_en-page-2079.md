

```markdown
Chapter 40 MIPI CSI GoBack


Register 40.3. CSI_HOST_CSI2_RESETN_REG (0x0008)

[Diagram: Register bitfield with label "reserved" and "CSI_HOST_CSI2_RESETN" at the right end, bits from 31 to 0 shown as circles, last few bits labeled "Reset"]
```
```markdown
CSI_HOST_CSI2_RESETN Configures whether to reset the internal logic of the MIPI CSI-2 host controller.
O: Reset
1: Release the reset

This register only affects the internal logic of the controller. It will not reset the configuration to default values.

(R/W)
```
```markdown
Register 40.4. CSI_HOST_PHY_SHUTDOWNZ_REG (0x0040)

[Diagram: Register bitfield with label "reserved" and "CSI_HOST_PHY_SHUTDOWNZ" at the right end, bits from 31 to 0 shown as circles, last few bits labeled "Reset"]
```
```markdown
CSI_HOST_PHY_SHUTDOWNZ Configures whether to enable the Shut-Down state of the RX D-PHY.
O: Enable
1: Disable

(R/W)
```