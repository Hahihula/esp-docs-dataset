

```markdown
Register 37.18. PPA_CK_DEFAULT_REG (0x0060)

| Bit | 31 | 25 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----|----|----|----|----|----|---|---|---|
|     |    |    | PPA_COLORKEY_FG_BG_REVERSE | PPA_COLORKEY_DEFAULT_R | PPA_COLORKEY_DEFAULT_G | (reserved) | PPA_COLORKEY_DEFAULT_B | Reset |
| Value | 0 | 0 | 0 | 0 | 0x0 | 0x0 | 0x0 |

PPA_COLORKEY_DEFAULT_B Configures the default B channel value of BLEND color-key. (R/W)
PPA_COLORKEY_DEFAULT_G Configures the default G channel value of BLEND color-key. (R/W)
PPA_COLORKEY_DEFAULT_R Configures the default R channel value of BLEND color-key. (R/W)

PPA_COLORKEY_FG_BG_REVERSE Configures the workflow when when a pixel is within the background color-key range but not within the foreground color-key range.
0: Output background pixel
1: Output foreground pixel
(R/W)
```