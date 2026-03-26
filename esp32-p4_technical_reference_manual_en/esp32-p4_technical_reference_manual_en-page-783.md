
```markdown
| No.| Chapter| Interrupt Source| Interrupt Source Mapping Register| Bit| Interrupt Status Register Name|
|----:|--------|------------------|-----------------------------------|----:|-------------------------------|
| 64 | GDMA Controller (GDMA-AHB, GDMA-AXI)| AXI_PDMA_IN_CH2_INTR| COREx_AXI_PDMA_IN_CH2_INT_MAP_REG| 0 | |
| 65 | GDMA Controller (GDMA-AHB, GDMA-AXI)| AXI_PDMA_OUT_CHO_INTR| COREx_AXI_PDMA_OUT_CHO_INT_MAP_REG| 1 | |
| 66 | GDMA Controller (GDMA-AHB, GDMA-AXI)| AXI_PDMA_OUT_CH1_INTR| COREx_AXI_PDMA_OUT_CH1_INT_MAP_REG| 2 | |
| 67 | GDMA Controller (GDMA-AHB, GDMA-AXI)| AXI_PDMA_OUT_CH2_INTR| COREx_AXI_PDMA_OUT_CH2_INT_MAP_REG| 3 | |
| 68 | RSA Accelerator (RSA)| RSA_INTR| COREx_RSA_INT_MAP_REG| 4 | |
| 69 | AES Accelerator (AES)| AES_INTR| COREx_AES_INT_MAP_REG| 5 | |
| 70 | SHA Accelerator (SHA)| SHA_INTR| COREx_SHA_INT_MAP_REG| 6 | COREx_INTR_STATUS_REG_2_REG|
| 71 | SHA Accelerator (SHA)| ECC_INTR| COREx_ECC_INT_MAP_REG| 7 | |
| 72 | ECDSA Digital Signature Peripheral (ECDSA_DS)| ECDSA_INTR| COREx_ECDSA_INT_MAP_REG| 8 | |
| 73 | Key Manager| KM_INTR| COREx_KM_INT_MAP_REG| 9 | |
| 74 | GPIO Matrix and IO MUX| GPIO_INTR0| COREx_GPIO_INTR0_MAP_REG| 10| |
| 75 | GPIO Matrix and IO MUX| GPIO_INTR1| COREx_GPIO_INTR1_MAP_REG| 11| |
| 76 | GPIO Matrix and IO MUX| GPIO_INTR2| COREx_GPIO_INTR2_MAP_REG| 12| |
| 77 | GPIO Matrix and IO MUX| GPIO_INTR3| COREx_GPIO_INTR3_MAP_REG| 13| |
| 78 | GPIO Matrix and IO MUX| GPIO_PAD_COMP_INTR| COREx_GPIO_PAD_COMP_INT_MAP_REG| 14| |
| 79 | System Registers (SYSREG)| CPU_INTR_FROM_CPU_0| COREx_CPU_INTR_FROM_CPU_0_MAP_REG| 15| |
| 80 | System Registers (SYSREG)| CPU_INTR_FROM_CPU_1| COREx_CPU_INTR_FROM_CPU_1_MAP_REG| 16| |
| 81 | System Registers (SYSREG)| CPU_INTR_FROM_CPU_2| COREx_CPU_INTR_FROM_CPU_2_MAP_REG| 17| |
| 82 | System Registers (SYSREG)| CPU_INTR_FROM_CPU_3| COREx_CPU_INTR_FROM_CPU_3_MAP_REG| 18| |
| 83 | n/a| reserved| reserved| 19| |
| 84 | SPI Controller (SPI)| FLASH_MSPI_INTR| COREx_FLASH_MSPI_INT_MAP_REG| 20| |
| 85 | MIPI CSI| CSI_BRIDGE_INTR| COREx_CSI_BRIDGE_INT_MAP_REG| 21| |
| 86 | MIPI DSI [to be added later]| DSI_BRIDGE_INTR| COREx_DSI_BRIDGE_INT_MAP_REG| 22| |
| 87 | MIPI CSI| CSI_INTR| COREx_CSI_INT_MAP_REG| 23| |
| 88 | MIPI DSI [to be added later]| DSI_INTR| COREx_DSI_INT_MAP_REG| 24| |
| 89 | Ethernet Media Access Controller (EMAC)| GMII_PHY_INTR| COREx_GMII_PHY_INT_MAP_REG| 25| |
| 90 | Ethernet Media Access Controller (EMAC)| LPI_INTR| COREx_LPI_INT_MAP_REG| 26| |
| 91 | Ethernet Media Access Controller (EMAC)| PMT_INTR| COREx_PMT_INT_MAP_REG| 27| |
| 92 | Ethernet Media Access Controller (EMAC)| ETH_MAC_INTR| COREx_ETH_MAC_INT_MAP_REG| 28| |
| 93 | USB 2.0 High-Speed OTG| USB_OTG_INTR| COREx_USB_OTG_INT_MAP_REG| 29| |
| 94 | USB 2.0 High-Speed OTG| USB_OTG_ENDP_MULTI_PROC_INTR| COREx_USB_OTG_ENDP_MULTI_PROC_INT_MAP_REG| 30| |
| 95 | JPEG Codec| JPEG_INTR| COREx_JPEG_INT_MAP_REG| 31| |
```