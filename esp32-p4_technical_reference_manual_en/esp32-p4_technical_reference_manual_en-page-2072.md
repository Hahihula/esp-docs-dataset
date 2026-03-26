

```markdown
| ERR_ECC_CORRECTED_VCn (n: 0-15) | Checksum error detected on virtual channel n | CSI_HOST_ST_ERR_ECC_CORRECTED_VCn (n: 0-15) |
| PHY_ERRSOTHS_n (n: 0-1)          | Start-of-transmission error (synchronization can still be achieved) on data lane n | CSI_HOST_ST_PHY_ERRSOTHS_n (n: 0-1)         |
| PHY_ERRESC_n (n: 0-1)            | Escape entry error (ULPS) on data lane n     | CSI_HOST_ST_PHY_ERRESC_n (n: 0-1)           |

**Note:**  
MIPI CSI does not support virtual channel interleaving. Before starting transmission, verify which virtual channel is in use. Additionally, read error information from the specified virtual channel to detect any errors. A reset is recommended for all errors in “*_FATAL_REG” registers.

## 40.6 Interrupts

ESP32-P4’s MIPI CSI can generate the CSI_INTR interrupt signal that will be sent to the **Interrupt Matrix**. The CSI_HOST_INT_ST_<group> registers report error conditions and trigger the CSI_INTR interrupt signal.

You can mask the interrupt pin by using the CSI_HOST_INT_MSK_<group> registers. All errors are masked by default. Set any bit of these registers to 1 to enable the specific error interrupt. The error asserts the respective bit in the CSI_HOST_INT_ST_<group> register. The CSI_HOST_INT_ST_<group> registers clear after a read operation.

Setting any bit of the Interrupt Force registers (CSI_HOST_INT_FORCE_<group>) to 1 triggers the corresponding interrupt without needing to activate the error conditions. These registers are for test purposes.

Figure40.6-1 shows the interrupt mechanism:
```