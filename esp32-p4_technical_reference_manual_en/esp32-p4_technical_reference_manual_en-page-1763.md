

```markdown
## 37.5.4.2 Filled Image Output

BLEND also supports filled image output. When this feature is enabled, only the output side of BLEND works, continuously outputting the filled image. The size and data of the filled image can be configured via `PPA_BLEND_TX_SIZE_REG` and `PPA_BLEND_TX_FIX_PIXEL`.

## 37.6 Interrupts

ESP32-P4’s PPA can generate the following interrupt signal that will be sent to the **Interrupt Matrix**.

*   `PPA_INTR`

The following interrupt sources can generate `PPA_INTR` interrupt signal:

*   `PPA_SRM_PARAM_CFG_ERR_INT`: Triggered when invalid parameters are configured in the SRM mode. You can acquire the specific error type through `PPA_SRM_PARAM_ERR_ST_REG`, as shown in Table 37.6-1.
*   `PPA_BLEND_PARAM_CFG_ERR_INT`: Triggered when invalid parameters are configured in the BLEND mode. You can acquire the specific error type through `PPA_BLEND_ST_REG`, as shown in Table 37.6-2.
*   `PPA_SRM_EOF_INT`: Triggered when SRM workflow reaches EOF.
*   `PPA_BLEND_EOF_INT`: Triggered when BLEND workflow reaches EOF.

Table 37.6-1. SRM Parameter Error Types

| Error Type                        | Details                                                                                                                                                                                                 |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `PPA_TX_DSCR_VB_ERR_ST`           | The sum of the vertical size of the output image block from SRM and the vertical offset Y specified in the output descriptor exceeds the total vertical size of the image configured in the output descriptor (VA) |
| `PPA_TX_DSCR_HB_ERR_ST`           | The sum of the horizontal size of the output image block from SRM and the vertical offset X specified in the output descriptor exceeds the total horizontal size of the image configured in the output descriptor (HA)   |
| `PPA_Y_RX_SCAL_EQUAL_O_ERR_ST`    | The vertical scaling factor for the input image block in SRM is set to 0                                                                                                                                 |
| `PPA_RX_DSCR_VB_ERR_ST`           | The sum of the vertical size VB and the vertical offset Y in the SRM input descriptor exceeds the overall vertical size VA in the output descriptor                                                                 |
| `PPA_YDST_LEN_TOO_SAMLL_ERR_ST`   | The vertical size of the image block after SRM scaling is 0. For example, if the vertical size of the image block is 14 and the vertical scaling factor is 1/16 without rotation, the scaled vertical size of the image block becomes 0 |
| `PPA_YDST_LEN_TOO_LARGE_ERR_ST`   | The vertical size of the image block after SRM scaling exceeds 8191                                                                                                                                          |
| `PPA_X_RX_SCAL_EQUAL_O_ERR_ST`    | The horizontal scaling factor for the input image block in SRM is 0                                                                                                                                          |

Continued on the next page...
```