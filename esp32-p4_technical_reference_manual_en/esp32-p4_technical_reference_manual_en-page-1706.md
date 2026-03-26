

```markdown
Register 36.62. ISP_AF_HSCALE_A_REG (0x0134)

| 31 | 28 | 27 |      | 16 | 15 | 12 | 11 | 0 |
|-----|-----|-----|------|----|----|----|----|---|
|     |     |     | (reserved) | ISP_AF_LPOINT_A | (reserved) | ISP_AF_RPOINT_A |
| 0   | 0   | 0   |        | 1                  | 0   | 0   | 0   | 128 Reset |

ISP_AF_RPOINT_A Configures the right boundary coordinate of AF statistical window A, recommended to be less than HNUM-1. (R/W)

ISP_AF_LPOINT_A Configures the left boundary coordinate of AF statistical window A, recommended to be greater than or equal to 2. (R/W)

Register 36.63. ISP_AF_VSCALE_A_REG (0x0138)

| 31 | 28 | 27 |      | 16 | 15 | 12 | 11 | 0 |
|-----|-----|-----|------|----|----|----|----|---|
|     |     |     | (reserved) | ISP_AF_TPOINT_A | (reserved) | ISP_AF_BPOINT_A |
| 0   | 0   | 0   |        | 1                  | 0   | 0   | 0   | 128 Reset |

ISP_AF_BPOINT_A Configures the bottom boundary coordinate of AF statistical window A, recommended to be less than HNUM-1. (R/W)

ISP_AF_TPOINT_A Configures the top boundary coordinate of AF statistical window A, recommended to be greater than or equal to 2. (R/W)

Register 36.64. ISP_AF_HSCALE_B_REG (0x013C)

| 31 | 28 | 27 |      | 16 | 15 | 12 | 11 | 0 |
|-----|-----|-----|------|----|----|----|----|---|
|     |     |     | (reserved) | ISP_AF_LPOINT_B | (reserved) | ISP_AF_RPOINT_B |
| 0   | 0   | 0   |        | 1                  | 0   | 0   | 0   | 128 Reset |

ISP_AF_RPOINT_B Configures the right boundary coordinate of AF statistical window B, recommended to be less than HNUM-1. (R/W)

ISP_AF_LPOINT_B Configures the left boundary coordinate of AF statistical window B, recommended to be greater than or equal to 2. (R/W)
```