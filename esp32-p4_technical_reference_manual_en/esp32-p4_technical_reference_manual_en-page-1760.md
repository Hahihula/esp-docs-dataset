

```markdown
| PPA_SRM_BK_SIZE_SEL | Pixel Format   | DMA2D_OUT_DSCR_PORT_BLK_H_CHx | DMA2D_OUT_DSCR_PORT_BLK_V_CHx |
|---------------------|----------------|-------------------------------|-------------------------------|
| 0                   | ARGB8888       |                               |                               |
|                     | RGB888         |                               |                               |
|                     | RGB565         | 34                            | 34                            |
|                     | GRAY           |                               |                               |
| 0                   | YUV422         | 36                            | 34                            |
| 0                   | YUV420         | 36                            | 36                            |
| 1                   | ARGB8888       |                               |                               |
|                     | RGB888         |                               |                               |
|                     | RGB565         | 18                            | 18                            |
|                     | GRAY           |                               |                               |
| 1                   | YUV422         | 20                            | 18                            |
| 1                   | YUV420         | 20                            | 20                            |

Note:
For optimal memory-access performance, use the default setting PPA_SRM_BK_SIZE_SEL = 0.
```

## 37.5.3 Scaling - Rotation - Mirroring (SRM)

### 37.5.3.1 Basic Functionality

SRM supports scaling, rotation, and mirroring. It first scales the image based on the origin point, then rotates it around the center point ($X_{middle}$, $Y_{middle}$), and finally mirrors it horizontally and vertically based on the center point ($X_{target}$, $Y_{target}$), as shown in Figure 37.5-4. Scaling, rotation, and mirroring parameters are all configured through registers:

*   PPA_SRM_SCAL_X_INT: Integer part of the horizontal scaling factor
*   PPA_SRM_SCAL_X_FRAG: Fractional part of the horizontal scaling factor
*   PPA_SRM_SCAL_Y_INT: Integer part of the vertical scaling factor
*   PPA_SRM_SCAL_Y_FRAG: Fractional part of the vertical scaling factor
*   PPA_SRM_ROTATE_ANGLE: Counterclockwise rotation angle
*   PPA_SRM_MIRROR_X: Enable horizontal mirroring
*   PPA_SRM_MIRROR_Y: Enable vertical mirroring
```