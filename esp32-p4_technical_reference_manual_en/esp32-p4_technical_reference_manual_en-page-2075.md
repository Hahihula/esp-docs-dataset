

```markdown
Chapter 40 MIPI CSI GoBack


*   Set `HP_SYS_CLKRST_RST_EN_CSI_HOST` to 0 to release the MIPI CSI reset.
*   Configure `HP_SYS_CLKRST_MIPI_CSI_DPHY_CLK_SRC_SEL` to select a proper clock source for the MIPI RX D-PHY configuration clock.
*   Set `HP_SYS_CLKRST_MIPI_CSI_DPHY_CFG_CLK_EN` to 1 to enable the MIPI RX D-PHY configuration clock.
*   Set `HP_SYS_CLKRST_RST_EN_CSI_BRG` to 1 to release the CSI_Bridge module of the ISP and reset the ISP.


### 40.71.2 MIPI RX D-PHY and MIPI Host Initialization

*   Clear `CSI_HOST_CSI2_RESETN` to reset the CSI_HOST controller logic.
*   Set `CSI_HOST_PHY_TESTCLR` to 1, then clear `CSI_HOST_PHY_TESTCLR` to reset the test code logic.
*   Configure the MIPI RX D-PHY frequency range in test code 0x44 using the MIPI RX D-PHY programming interface.
*   Configure `CSI_HOST_N_LANES` to define the number of active lanes in the system.
*   Set `CSI_HOST_PHY_SHUTDOWNZ` and `CSI_HOST_DPHY_RSTZ` to 1 to release the MIPI RX D-PHY from the reset state.
*   Set the corresponding bit in the `CSI_HOST_INT_MSK_*_REG` register to 1 to enable the error interrupt.
*   Configure the descrambler function if needed.
*   Set `CSI_HOST_CSI2_RESETN` to 1 to release the CSI_HOST reset.
*   Wait until `CSI_HOST_PHY_STOPSTATEDATA_n` and `CSI_HOST_PHY_STOPSTATECLK` are 1.
*   Start the camera image capture.


### 40.7.2 Stop High-Speed Data Reception

*   Disable related channels in . Wait until is disabled. Refer to Chapter 5 VDMA Controller (VDMA).
*   Reset the ISP. Refer to Chapter 36 Image Signal Processor (ISP).
*   Set `HP_SYS_CLKRST_RST_EN_CSI_HOST` to 1 to reset the MIPI CSI.
```