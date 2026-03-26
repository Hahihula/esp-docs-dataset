

```markdown
## Register 37.30. PPA_DEBUG_CTRL0_REG (0x0090)

PPA_DBG_REPLACE_SEL Configures where the replacement pixel is inserted.

- 0: No replacement
- 1: SRM RX input
- 2: SRM interpolation output
- 3: SRM TX output
- 4: BLEND foreground input
- 5: BLEND background input
- 6: BLEND output

(R/W)

## Register 37.31. PPA_DEBUG_CTRL1_REG (0x0094)

PPA_DBG_REPLACE_DATA Configures the replacement pixel value. (R/W)

## Register 37.32. PPA_RGB2GRAY_REG (0x0098)

PPA_RGB2GRAY_B Configures the coefficient for B in RGB to GRAY conversion. (R/W)
PPA_RGB2GRAY_G Configures the coefficient for G in RGB to GRAY conversion. (R/W)
PPA_RGB2GRAY_R Configures the coefficient for R in RGB to GRAY conversion. (R/W)
```