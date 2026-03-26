

```markdown
Register 40.5. CSI_HOST_DPHY_RSTZ_REG (0x0044)

31 | [reserved] | CSI_HOST_DPHY_RSTZ
----------------------------------------------------------------------------------------------------
0 | ... | Reset

CSI_HOST_DPHY_RSTZ Configures whether to reset the RX D-PHY digital circuitry.
O: Reset
1: Release the reset
(R/W)
```

```markdown
Register 40.6. CSI_HOST_PHY_RX_REG (0x0048)

31 | [reserved] | CSI_HOST_PHY_RXULPSESC_1 | CSI_HOST_PHY_RXULPSESC_0
----------------------------------------------------------------------------------------------------
0 | ... | Reset

CSI_HOST_PHY_RXULPSESC_n (n: 0-1) Represents whether data lane n has entered the Ultra Low Power State.
O: Entered
1: Not entered
(RO)

CSI_HOST_PHY_RXULPSCLKNOT Represents whether RX D-PHY clock lane has entered the Ultra Low Power State.
O: Entered
1: Not entered
(RO)

CSI_HOST_PHY_RXCLKACTIVEHS Represents whether RX D-PHY clock lane is actively receiving a DDR clock.
O: Not actively receiving
1: Actively receiving
(RO)
```