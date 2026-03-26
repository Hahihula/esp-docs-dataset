

```markdown
| PPA_SRM_RX_ALPHA_INV | PPA_SRM_RX_ALPHA_MOD | Output |
|-----------------------|----------------------|--------|
|                       | 00/11                | Original Alpha value |
| O                     |                      | The configuration value of `PPA_SRM_RX_FIX_ALPHA` |
|                       | 10                   | The high 8 bits of the value obtained by multiplying the original Alpha value with `PPA_SRM_RX_FIX_ALPHA` |
|                       | 00/11                | The value obtained by subtracting the original Alpha value from 255 |
| 1                     |                      | The configuration value of `PPA_SRM_RX_FIX_ALPHA` |
|                       | 10                   | The high 8 bits of the value obtained by multiplying the result of subtracting the original Alpha value from 255 by `PPA_SRM_RX_FIX_ALPHA` |

Note that when the input or output format is YUV, further configuration of YUV to RGB color conversion is required.

When the input format is YUV420, the input YUV data range needs to be configured as full-range or limit-range via the `PPA_YUV_RX_RANGE` field, and the protocol used for YUV to RGB conversion needs to be configured as BT601 or BT709 via the `PPA_YUV2RGB_PROTOCOL` field. The conversion formulas are as follows:

*   `YUVfull` to `YUVlimit`
    -  `Ylimit = (220/256) * Yfull + 16`
    -  `Ulimit = (225/256) * Ufull + 16`
    -  `Vlimit = (225/256) * Vfull + 16`

*   `YUVlimit` to RGB in BT601
    -  `R = (298/256) * Ylimit + (409/256) * Ulimit - (56906/256)`
    -  `G = (298/256) * Ylimit - (100/256) * Ulimit - (208/256) * Vlimit + (34707/256)`
    -  `B = (298/256) * Ylimit + (516/256) * Ulimit - (70836/256)`
```