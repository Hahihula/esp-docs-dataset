

```markdown
Register 36.65. ISP_AF_VSCALE_B_REG (0x0140)

| 31 | 28 | 27 |        | 16 | 15 | 12 | 11 |      | 0 |
|-----|----:|----:|--------|----:|----:|----:|----:|------|---|
| 0   | 0   | 0   | (reserved) |     |     | 0   | 0   | 0    | Reset |

ISP_AF_BPOINT_B Configures the bottom boundary coordinate of AF statistical window B, recommended to be less than HNUM-1. (R/W)

ISP_AF_TPOINT_B Configures the top boundary coordinate of AF statistical window B, recommended to be greater than or equal to 2. (R/W)


Register 36.66. ISP_AF_HSCALE_C_REG (0x0144)

| 31 | 28 | 27 |        | 16 | 15 | 12 | 11 |      | 0 |
|-----|----:|----:|--------|----:|----:|----:|----:|------|---|
| 0   | 0   | 0   | (reserved) |     |     | 0   | 0   | 0    | Reset |

ISP_AF_RPOINT_C Configures the right boundary coordinate of AF statistical window C, recommended to be less than HNUM-1. (R/W)

ISP_AF_LPOINT_C Configures the left boundary coordinate of AF statistical window C, recommended to be greater than or equal to 2. (R/W)


Register 36.67. ISP_AF_VSCALE_C_REG (0x0148)

| 31 | 28 | 27 |        | 16 | 15 | 12 | 11 |      | 0 |
|-----|----:|----:|--------|----:|----:|----:|----:|------|---|
| 0   | 0   | 0   | (reserved) |     |     | 0   | 0   | 0    | Reset |

ISP_AF_BPOINT_C Configures the bottom boundary coordinate of AF statistical window C, recommended to be less than HNUM-1. (R/W)

ISP_AF_TPOINT_C Configures the top boundary coordinate of AF statistical window C, recommended to be greater than or equal to 2. (R/W)
```