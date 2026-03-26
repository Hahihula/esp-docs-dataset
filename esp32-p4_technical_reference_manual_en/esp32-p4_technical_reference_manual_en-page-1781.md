

```markdown
|31|PPA_BLEND0_RX_FIX_ALPHA_PPA_BLEND1_RX_FIX_ALPHA_PPA_BLEND0_RX_ALPHA_INV_PPA_BLEND1_RX_ALPHA_MOD_PPA_BLEND0_RX_FIX_ALPHA_PPA_BLEND1_RX_FIX_ALPHA_PPA_BLEND0_RX_ALPHA_MOD_PPA_BLEND1_RX_ALPHA_MOD_PPA_BLEND0_RX_ALPHA_INV_PPA_BLEND1_RX_ALPHA_INV|22|PPA_BLEND0_RX_FIX_ALPHA_PPA_BLEND1_RX_FIX_ALPHA_PPA_BLEND0_RX_ALPHA_MOD_PPA_BLEND1_RX_ALPHA_MOD_PPA_BLEND0_RX_ALPHA_INV_PPA_BLEND1_RX_ALPHA_INV|21|reserved(1)|20|reserved(1)|19|reserved(1)|18|reserved(1)|17|reserved(1)|16|reserved(1)|15|reserved(1)|8|reserved(1)|7|reserved(1)|0|reserved(1)|
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|-------------|----|
||0 0 0 0 0 0 0 0 0 0 0 0 128|Reset|

PPA_BLENDO_RX_FIX_ALPHA (R/W) Configures the Alpha channal value of the BLEND background layer.

PPA_BLEND1_RX_FIX_ALPHA Configures the Alpha channal value of the BLEND foreground layer. (R/W)

PPA_BLENDO_RX_ALPHA_MOD Configures the Alpha mode of BLEND background layer data.
1: Use the value of PPA_BLENDO_RX_FIX_ALPHA
2: Use the value of the higher eight bits of the original Alpha value multiplied by PPA_BLENDO_RX_FIX_ALPHA
Others: Use the value of the original Alpha value (R/W)

PPA_BLEND1_RX_ALPHA_MOD Configures the Alpha mode of BLEND foreground layer data.
1: Use the value of PPA_BLEND1_RX_FIX_ALPHA
2: Use the value of the higher eight bits of the original Alpha value multiplied by PPA_BLEND1_RX_FIX_ALPHA
Others: Use the value of the original Alpha value (R/W)

PPA_BLENDO_RX_ALPHA_INV Configures whether to invert the original Alpha value of the BLEND background layer data.
0: Not invert
1: Invert to 255 minus the original Alpha value
For data formats without Alpha channels, the original Alpha value is 255. (R/W)

PPA_BLEND1_RX_ALPHA_INV Configures whether to invert the original Alpha value of the BLEND foreground layer data.
0: Not invert
1: Invert to 255 minus the original Alpha value
For data formats without Alpha channels, the original Alpha value is 255. (R/W)
```