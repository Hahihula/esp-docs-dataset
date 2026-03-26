

```markdown
Register 36.94. ISP_CROP_Y_CAPTURE_REG (0x0248)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 24  | ISP_CROP_Y_END       |
| 23  |                     |
| 12  |                     |
| 11  |                     |
| 0   | Reset               |

ISP_CROP_Y_START Configures the start coordinate in the Y direction. (R/W)
ISP_CROP_Y_END Configures the end coordinate in the Y direction. (R/W)

Register 36.95. ISP_CROP_X_CAPTURE_REG (0x024C)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 24  | ISP_CROP_X_END       |
| 23  |                     |
| 12  |                     |
| 11  |                     |
| 0   | Reset               |

ISP_CROP_X_START Configures the start coordinate in the X direction. (R/W)
ISP_CROP_X_END Configures the end coordinate in the X direction. (R/W)

Register 36.96. ISP_CROP_ERR_ST_REG (0x0250)

| Bit | Description                                 |
|-----|---------------------------------------------|
| 31  | (reserved)                                  |
| 30  | ISP_CROP_Y_MISMATCH                         |
| 29  | Represents an error where the configured CROP Y coordinate exceeds the image boundary. (RO)
| 28  | ISP_CROP_X_MISMATCH                         |
| 27  | Represents an error where the configured CROP X coordinate exceeds the image boundary. (RO)
| 26  | ISP_CROP_Y_END_EVEN                         |
| 25  | Represents an error where the Y-direction end coordinate is even. (RO)
| 24  | ISP_CROP_X_END_EVEN                         |
| 23  | Represents an error where the X-direction end coordinate is even. (RO)
| 22  | ISP_CROP_Y_START_ODD                        |
| 21  | Represents an error where the Y-direction start coordinate is odd. (RO)
| 20  | ISP_CROP_X_START_ODD                        |
| 19  | Represents an error where the X-direction start coordinate is odd. (RO)
| 18-0| Reset                                      |
```