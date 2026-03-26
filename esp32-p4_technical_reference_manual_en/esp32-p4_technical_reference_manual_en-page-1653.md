

```markdown
| CSI_BRIG_DISCARD_INT | When any frame is discarded in CSI_Bridge | csi_bridge_interrupt |
|------------------------|-------------------------------------------|-----------------------|
| CSI_BRIG_VADR_NUM_LT_INT | When CSI_BRIG_VADR_NUM is less than the actual value | csi_bridge_interrupt |
| CSI_BRIG_VADR_NUM_GT_INT | When CSI_BRIG_VADR_NUM is greater than the actual value | csi_bridge_interrupt |

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

Each interrupt source can be configured by a common set of registers that are described in Section *Interrupt Configuration Registers*. The specific registers can be found in Section 36.8 Register Summary.

## 36.7 Programming Procedures

### 36.7.1 ISP Clock Reset Configuration

1. Enable the bus clock for the ISP and CSI_Bridge modules;

   - Set `HP_SYS_CLKRST_CSI_BRG_SYS_CLK_EN` to 1 to activate the clock for ISP and CSI_Bridge.

2. Configure the working clock for ISP;

   - Choose the clock source via `HP_SYS_CLKRST_ISP_CLK_SRC_SEL`
   - Configure the clock divisor via `HP_SYS_CLKRST_ISP_CLK_DIV_NUM`
   - Set `HP_SYS_CLKRST_ISP_CLK_EN` to 1 to activate the ISP working clock

3. Reset ISP and CSI_Bridge modules.

   - Set `HP_SYS_CLKRST_RST_EN_CSI_BRG` to 1 and then 0 to reset ISP and CSI_Bridge

### 36.7.2 CSI_Bridge Configuration

1. Set the width and height of the image via `CSI_BRIG_HADR_NUM` and `CSI_BRIG_VADR_NUM`. The width is measured in "64-bit" units, and the height is measured in rows;

2. Set the valid range for DATA_TYPE via `CSI_BRIG_DATA_TYPE_MIN` and `CSI_BRIG_DATA_TYPE_MAX`;

3. Specify the burst length via `CSI_BRIG_DMA_BURST_LEN`. Ensure that this value matches the SRC_MSIZE (length per burst) and SRC_TR_WIDTH (data width) of the corresponding VDMA channel. The data width for CSI_Bridge is measured in "64-bit" units;

4. If the image is transferred in multiple blocks, specify the maximum number of VDMA bursts per block via `CSI_BRIG_DMAPBLK_SIZE`;

5. Enable CSI_Bridge by writing 1 to `CSI_BRIG_CSI_BRIG_EN`.
```