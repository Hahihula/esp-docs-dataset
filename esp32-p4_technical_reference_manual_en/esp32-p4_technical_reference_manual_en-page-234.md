

```markdown
|2|UHCI|
|---|----|
|3|I2SO|
|4|I2S1|
|5|I2S2|
|6~7|Dummy-6 ~ 7|
|8|ADC|
|9|Dummy-9|
|10|RMT|
|11~15|Dummy-11 ~ 15|
|16~63|Invalid|

Table 4.4-2. GDMA-AXI Selecting Peripherals via Register Configuration

|AXI_DMA_PERI_IN_SEL_CHn|Peripheral|
|---|----------|
|AXI_DMA_PERI_OUT_SEL_CHn||
|0|LCD or CAM|
|1|SPI2|
|2|SPI3|
|3|PARLIO|
|4|AES|
|5|SHA|
|6~15|Dummy-6 ~ 15|
|16~63|Invalid|

## 4.4.3 Memory-to-Memory Data Transfer

The GDMA controller also allows memory-to-memory data transfer. Such data transfer can be enabled by setting AHB/AXI_DMA_MEM_TRANS_EN_CHn, which connects the output of transmit channel n to the input of receive channel n. Note that a transmit channel is only connected to the receive channel with the same number (n), and AHB/AXI_DMA_PERI_IN_SEL_CHn and AHB/AXI_DMA_PERI_OUT_SEL_CHn should be configured to the same value corresponding to "Dummy".

GDMA-AHB only supports memory-to-memory data transfer on channels 1 and 2, and the AXI_DMA_PERI_IN_SEL_CHn and AXI_DMA_PERI_OUT_SEL_CHn (n = 1 ~ 2) fields need to be configured to fixed values. When using channel 1, configure both fields to 11; when using channel 2, configure both fields to 12.

## 4.4.4 Enabling GDMA

The software uses the GDMA controller through linked lists. When the GDMA controller receives data, software loads an inlink, configures the AHB/AXI_DMA_INLINK_ADDR_CHn field with the address of the first receive descriptor, and sets the AHB/AXI_DMA_INLINK_START_CHn bit to enable GDMA. When the GDMA controller transmits data, software loads an outlink, prepares data to be transmitted, configures the AHB/AXI_DMA_OUTLINK_ADDR_CHn field with address of the first transmit descriptor, and sets the AHB/AXI_DMA_OUTLINK_START_CHn bit to enable GDMA. The AHB/AXI_DMA_INLINK_START_CHn bit and AHB/AXI_DMA_OUTLINK_START_CHn bit are cleared automatically by hardware.
```