

```markdown
2. Configure the EMAC system clock by setting HP_SYS_CLKRST_EMAC_SYS_CLK_EN to 1.
3. Configure the PHY interface clock:

• RMII interface: select the RMII interface by configuring HP_SYS_PHY_INTF_SEL to 4.

    – Select RMII reference clock source:

        * Reference clock sourced from the external crystal:
            • Configure HP_SYS_CLKRST_PAD_EMAC_REF_CLK_EN to disable PAD_EMAC_REF_CLK outputted to GPIO.
            • Configure HP_SYS_CLKRST_REF_50M_CLK_EN to disable PLL_F50M_CLK.

        * Reference clock sourced from ESP32-P4:
            • Configure HP_SYS_CLKRST_PAD_EMAC_REF_CLK_EN to enable PAD_EMAC_REF_CLK outputted to GPIO.
            • Configure HP_SYS_CLKRST_REF_50M_CLK_DIV_NUM to specify the clock divisor for PLL_F50M_CLK.
            • Configure HP_SYS_CLKRST_REF_50M_CLK_EN to enable PLL_F50M_CLK.

        – Configure HP_SYS_CLKRST_EMAC_RMII_CLK_SRC_SEL to specify the clock source of EMAC_RMII_CLK as PAD_EMAC_TXRX_CLK;

        – Configure HP_SYS_CLKRST_EMAC_RX_CLK_SRC_SEL to specify the clock source of EMAC_RX_CLK as PAD_EMAC_TXRX_CLK;

        – Configure HP_SYS_CLKRST_EMAC_RX_CLK_DIV_NUM to specify the clock divisor for EMAC_RX_CLK according to the EMAC line speed (10 Mbit/s or 100 Mbit/s);

        – Configure HP_SYS_CLKRST_EMAC_TX_CLK_SRC_SEL to specify the clock source of EMAC_TX_CLK as PAD_EMAC_TXRX_CLK;

        – Configure HP_SYS_CLKRST_EMAC_TX_CLK_DIV_NUM to specify the clock divisor for EMAC_TX_CLK according to the EMAC line speed (10 Mbit/s or 100 Mbit/s);

        – Configure LP_AONCLKRST_HP_PAD_EMAC_TXRX_CLK_EN to enable the clock from IO pin PAD_EMAC_TXRX_CLK;

        – Configure HP_SYS_CLKRST_EMAC_RMII_CLK_EN to enable EMAC_RMII_CLK;

        – Configure HP_SYS_CLKRST_EMAC_RX_CLK_EN to enable EMAC_RX_CLK;

        – Configure HP_SYS_CLKRST_EMAC_TX_CLK_EN to enable EMAC_TX_CLK;

    • MII interface: select the MII interface by configuring HP_SYS_PHY_INTF_SEL to 0.

        – Configure HP_SYS_CLKRST_EMAC_RX_CLK_SRC_SEL to specify EMAC_RX_CLK as PAD_EMAC_RX_CLK;

        – Configure HP_SYS_CLKRST_EMAC_RX_CLK_DIV_NUM to specify the clock divisor for EMAC_RX_CLK according to the EMAC line speed (10 Mbit/s or 100 Mbit/s);

        – Configure HP_SYS_CLKRST_EMAC_TX_CLK_SRC_SEL to specify EMAC_TX_CLK as PAD_EMAC_TX_CLK;
```