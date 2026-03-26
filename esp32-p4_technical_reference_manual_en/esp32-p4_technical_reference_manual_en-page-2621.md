

```markdown
Figure 52.4-6. RMII Clock
```

## 52.4.4.3 Station Manager Agent (SMA) Interface

As Figure 52.4-3 and Figure 52.4-5 show, the MAC uses MDC and MDIO signals to transfer control and data information to the PHY. The MDC clock is generated from the application clock through a clock divider and operates at a maximum frequency of 2.5 MHz. The MDIO data signal transfers to and from PHY synchronously with the MDC clock signal. Meanwhile, the PHY transmits register data.

*   Read a PHY register:
    -   Read `MIIBUSY` until the MII is in an idle state.
    -   Configure `MIIDEV` to specify the PHY device to access.
    -   Configure `MIIREG` to specify the address of the PHY register to access.
    -   Configure `MIICSRCLK` to set the APB clock frequency.
    -   Set `MIIWRITE` to 0 for read access.
    -   Read `MIIBUSY` until the MII is in an idle state.
    -   Read `EMACMIIDATA_REG` to retrieve the value of the PHY register.

*   Write a PHY register:
    -   Read `MIIBUSY` until the MII is in an idle state.
    -   Configure `EMACMIIDATA_REG` to set the value to be written to the PHY register.
    -   Configure `MIIDEV` to specify the PHY device to access.
    -   Configure `MIIREG` to specify the address of the PHY register to access.
    -   Configure `MIICSRCLK` to set the APB clock frequency.
```