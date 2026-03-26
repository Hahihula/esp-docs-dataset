

```markdown
Register 54.21. SDHOST_CARDTHRCTL_REG (0x0100)

SDHOST_CARDRDTHREN_REG Configures whether to enable card read threshold.
- 0: Not enable
- 1: Enable
(R/W)

SDHOST_CARDCLRINTEN_REG Configures whether to enable busy clear interrupt generation.
- 0: Not enable
- 1: Enable
(R/W)

SDHOST_CARDTHRESHOLD_REG Configures the card read threshold. Measurement unit: byte.
This field is valid only when SDHOST_CARDRDTHREN_REG is set to 1.
The value should be less than the FIFO size 512.(R/W)
```

```markdown
Register 54.22. SDHOST_EMMCDDR_REG (0x010C)

SDHOST_HALFFSTARTBIT_REG Configures the start bit detection mechanism duration of start bit.
Each bit refers to one card. Set this bit to 1 for eMMC4.5 and above, set to 0 for SD applications.
For eMMC4.5, start bit can be:
- 0: Full cycle
- 1: Less than one full cycle
(R/W)
```