

```markdown
Register 5.5. DMAC_RESETO_REG (0x0058)

DMAC_DMAC_RST Configures whether to reset VDMA. Software writes 1 to this field to reset VDMA and polls this field to see if it is 0. VDMA resets all the modules except the APB slave interface module and clears this field to 0.
Note: Software is not allowed to write 0 to this field.
(R/W)
```

```markdown
Register 5.6. DMAC_LOWPOWER_CFGO_REG (0x0060)

DMAC_GBL_CSLP_EN Configures whether to enable global low-power feature.
O: Disable
1: Enable
(R/W)

DMAC_CHNL_CSLP_EN Configures whether to enable low-power feature for DMA channels.
O: Disable
1: Enable
(R/W)

DMAC_SBIU_CSLP_EN SBIU Configures whether to enable low-power feature for slave bus interface.
O: Disable
1: Enable
(R/W)

DMAC_MXIF_CSLP_EN Configures whether to enable low-power feature for AXI master interface.
O: Disable
1: Enable
(R/W)
```