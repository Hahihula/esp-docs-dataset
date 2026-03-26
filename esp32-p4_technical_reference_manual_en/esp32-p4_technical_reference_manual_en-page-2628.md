

```markdown
- Configure HP_SYS_CLKRST_EMAC_TX_CLK_DIV_NUM to specify the clock divisor for EMAC_TX_CLK according to the EMAC line speed (10 Mbit/s or 100 Mbit/s);
- Configure LP_AONCLKRST_HP_PAD_EMAC_RX_CLK_EN to enable the clock from IO pin PAD_EMAC_RX_CLK;
- Configure LP_AONCLKRST_HP_PAD_EMAC_TX_CLK_EN to enable the clock from IO pin PAD_EMAC_TX_CLK;
- Configure HP_SYS_CLKRST_EMAC_RX_CLK_EN to enable EMAC_RX_CLK;
- Configure HP_SYS_CLKRST_EMAC_TX_CLK_EN to enable EMAC_TX_CLK;

## 52.5.2 EMAC Initial Configuration

Initialize EMAC_DMA:

*   Reset EMAC by setting SW_RST to 1.
*   Wait for the completion of reset until reading 0 from SW_RST, which indicates that the reset is done.
*   Read AHB_ST; a value of 0 indicates that all AHB bus transactions have been completed.
*   Configure the AHB bus mode for EMAC_DMA via DMABUSMODE_REG.
*   Prepare the linked list and configure the linked list base address via DMARXBASEADDR_REG and DMATXBASEADDR_REG.
*   Configure the operating mode for EMAC_DMA and EMAC_MTL via DMAOPERATION_MODE_REG.
*   Configure whether to enable DMA interrupts via DMAIN_EN_REG.

Initialize EMAC_CORE:

*   Read EMACMIADDR_REG and EMACMIIDATA_REG for the PHY’s connection status, operating frequency, and operating mode.
*   Configure EMACADDROHIGH_REG and EMACADDROLOW_REG to specify the MAC address.
*   Configure EMACFF_REG to select the packet filtering mode.
*   Configure EMACFC_REG for flow control.
*   Configure whether to mask MAC interrupts via EMACINTMASK_REG.
*   Configure the MAC’s operating mode for transmission and reception via EMACCONFIG_REG.

## 52.5.3 Starting Transmission

*   Start EMAC_DMA transmission by setting START_STOP_TRANSMISSION_COMMAND to 1.
*   Start EMAC_CORE transmission by setting EMACTX to 1.
*   Detect the TRANS_INT interrupt if enabled, and wait for the frame transmission to complete.

## 52.5.4 Starting Reception

*   Start EMAC_DMA reception by setting START_STOP_RX to 1.
```