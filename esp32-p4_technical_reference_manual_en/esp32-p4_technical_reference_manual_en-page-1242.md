

```markdown
Chapter 20 System Registers (SYSREG)

GoBack

20.2.1.6 HP L2MEM ECC Check Configuration

ESP32-P4's has implemented the Error Correction Code (ECC) check in HP L2MEM (including L2RAM and cache) to correct one-bit memory flip error.

This feature can be configured and controlled via the following registers:

*   `HP_SYSTEM_L2_MEM_L2_RAM_ECC_REG` and `HP_SYSTEM_L2_MEM_L2_CACHE_ECC_REG`: write 1 to enable the ECC check for L2MEM and cache respectively.
*   `HP_SYSTEM_L2_MEM_REFRESH_REG`: configures the initialization of HP L2MEM before enabling the ECC check.
*   Interrupt (`L2_MEM_ECC_ERR_INT`) related registers:
    *   `HP_SYSTEM_L2_MEM_INT_RAW_REG`: the raw interrupt status of `L2_MEM_ECC_ERR_INT`
    *   `HP_SYSTEM_L2_MEM_INT_ST_REG`: the masked interrupt status of `L2_MEM_ECC_ERR_INT`
    *   `HP_SYSTEM_L2_MEM_INT_ENA_REG`: write 1 to enable `L2_MEM_ECC_ERR_INT`
    *   `HP_SYSTEM_L2_MEM_INT_CLR_REG`: write 1 to clear `L2_MEM_ECC_ERR_INT`
*   `HP_SYSTEM_L2_MEM_INT_RECORD1_REG`: records information when `L2_MEM_ECC_ERR_INT` occurs.
*   `HP_SYSTEM_L2_MEM_ERR_RESP_CTRL_REG`: write 1 so HP L2MEM reports ECC error to HP CPU and triggers exception.

For detailed configuration steps, please refer to Chapter 7 System and Memory.

20.2.1.7 BitScrambler Configuration

ESP32-P4 has some peripherals that support DMA. These peripherals sometimes need BitScramblers to change the format of data before communicating with DMA.

Configure `HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG` to attach such a peripheral to the RX and TX channels of bitscamblers respectively.

For detailed configuration steps, please refer to Chapter 59 BitScrambler.

For a list of DMA-capable peripherals, please refer to Chapter 10 Reset and Clock.

20.2.1.8 Ethernet MAC Control

ESP32-P4 can send and receive data via Ethernet MAC (Media Access Controller) according to the IEEE 802.3 standard.

The control and configuration registers are:

*   `HP_SYSTEM_GMAC_CTRL0_REG`
*   `HP_SYSTEM_GMAC_CTRL1_REG`
*   `HP_SYSTEM_GMAC_CTRL2_REG`

For details, please refer to Chapter 52 Ethernet Media Access Controller (EMAC).
```