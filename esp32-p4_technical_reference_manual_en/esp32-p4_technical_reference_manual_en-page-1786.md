

```markdown
Register 3719. PPA_SRM_SCAL_ROTATE_REG (0x0064)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 30  | PPA_SRM_MIRROR_Y              | Configures whether to enable the vertical mirroring for SRM.                |
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                       |
| 29  | PPA_SRM_MIRROR_X              | Configures whether to enable the horizontal mirroring for SRM.               |
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                       |
| 28  | PPA_SRM_ROTATE_START          | Write 1 to enable SRM. (WT)                                                 |
| 27  | PPA_SCAL_ROTATE_RST           | Configures whether to reset SRM.                                            |
|     |                                | O: Release reset                                                            |
|     |                                | 1: Reset                                                                     |
|     |                                | (R/W)                                                                       |
| 26  | PPA_SRM_ROTATE_ANGLE          | Configures the counterclockwise rotation angle for the SRM.                  |
|     |                                | 0: 0 degree                                                                  |
|     |                                | 1: 90 degree                                                                 |
|     |                                | 2: 180 degree                                                                |
|     |                                | 3: 270 degree                                                                |
|     |                                | (R/W)                                                                       |
| 25  | PPA_SRM_SCAL_Y_FRAG           | Configures the fragment part of the vertical scaling factor for SRM.         |
| 24  | PPA_SRM_SCAL_Y_INT            | Configures the integer part of the vertical scaling factor for SRM. (R/W)     |
| 23  | PPA_SRM_SCAL_X_FRAG           | Configures the fragment part of the horizontal scaling factor for SRM.       |
| 22  | PPA_SRM_SCAL_X_INT            | Configures the integer part of the horizontal scaling factor for SRM. (R/W)   |
|     |                                |                                                                             |
| Reset |                              | 1                                                                            |
```

PPA_SRM_SCAL_X_INT Configures the integer part of the horizontal scaling factor for SRM. (R/W)

PPA_SRM_SCAL_X_FRAG Configures the fragment part of the horizontal scaling factor for SRM. (R/W)

PPA_SRM_SCAL_Y_INT Configures the integer part of the vertical scaling factor for SRM. (R/W)

PPA_SRM_SCAL_Y_FRAG Configures the fragment part of the vertical scaling factor for SRM. (R/W)

PPA_SRM_ROTATE_ANGLE Configures the counterclockwise rotation angle for the SRM.
0: 0 degree
1: 90 degree
2: 180 degree
3: 270 degree
(R/W)

PPA_SCAL_ROTATE_RST Configures whether to reset SRM.

O: Release reset
1: Reset
(R/W)

PPA_SCAL_ROTATE_START Write 1 to enable SRM. (WT)

PPA_SRM_MIRROR_X Configures whether to enable the horizontal mirroring for SRM.
0: Disable
1: Enable
(R/W)

PPA_SRM_MIRROR_Y Configures whether to enable the vertical mirroring for SRM.
0: Disable
1: Enable
(R/W)
```