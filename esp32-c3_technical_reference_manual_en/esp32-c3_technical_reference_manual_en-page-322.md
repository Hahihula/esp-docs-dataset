

```markdown
| Buses | Environment | Configuration Registers                                                                                      | Instruction Region instr_region_0 | instr_region_1 | instr_region_2 | Access |
|-------|-------------|--------------------------------------------------------------------------------------------------------------|-----------------------------------|----------------|---------------|--------|
| IBUS  | Privileged   | PMS_CORE_X_IRAMO_PMS_CONSTRN_2_REG                                                                          | [2:0]                             | [5:3]          | [8:6]         | X/W/R  |
|       | Unprivileged | PMS_CORE_X_IRAMO_PMS_CONSTRN_1_REG                                                                          | [2:0]                             | [5:3]          | [8:6]         | X/W/R  |
| DBUS  | Privileged   | PMS_Core_X_DRAMO_PMS_CONSTRN_1_REG                                                                           | [13:12]^A                        |                |               | W/R    |
|       | Unprivileged |                                                                                                              | [1:0]^A                           |                |               | W/R    |
| GDMA C| XX Peripherals D | PMS_DMA_APBPERI_XX_PMS_CONSTRN_1_REG                                                                         | [1:0]^B                           |                |               | W/R    |

^A Configure DBUS' access to the Instruction Region. However, it's recommended to configure these bits to 0.
^B Configure GDMA's access to the Instruction Region. However, it's recommended to configure these bits to 0.
^C GDMA doesn't support the privileged environment and unprivileged environment.
^D ESP32-C3 has 6 peripherals, including SPI2, UCHIO, I2S, AES, SHA, ADC, which can access Internal SRAM1 via GDMA.

Each peripherals can be configured with different access to the Internal SRAM1 independently.

| Buses | Environment | Configuration Registers                                                                                      | Data Region data_region_0 | data_region_1 | data_region_2 | Access |
|-------|-------------|--------------------------------------------------------------------------------------------------------------|---------------------------|---------------|---------------|--------|
| IBUS  | Privileged   | PMS_CORE_X_IRAMO_PMS_CONSTRN_2_REG                                                                          | [11:9]^A                  |               |               | X/W/R  |
|       | Unprivileged | PMS_CORE_X_IRAMO_PMS_CONSTRN_1_REG                                                                          | [11:9]^A                  |               |               | X/W/R  |
| DBUS  | Privileged   | PMS_Core_X_DRAMO_PMS_CONSTRN_1_REG                                                                           | [3:2]                     | [5:4]         | [7:6]         | W/R    |
|       | Unprivileged |                                                                                                              | [15:14]                   | [17:16]       | [19:18]       | W/R    |
| GDMA B| XX Peripherals C | PMS_DMA_APBPERI_XX_PMS_CONSTRN_1_REG                                                                         | [3:2]                     | [5:4]         | [7:6]         | W/R    |

^A Configure IBUS' access to the Data Region. However, it's recommended to configure these bits to 0.
^B GDMA doesn't support the privileged environment and the unprivileged environment.
^C ESP32-C3 has six peripherals, including SPI2, UCHIO, I2S, AES, SHA, ADC, which can access Internal SRAM1 via GDMA.

Each peripheral can be configured with different access to the Internal SRAM1 independently.

For details on how to configure the split lines, see Section 14.4.2.2.
```

```markdown
Note:
If enabled, the permission control module watches all the memory access and fires the panic handler if a permission violation is detected. This feature automatically splits the SRAM memory into data and instruction segments and sets Read/Execute permissions for the instruction part (below given splitting address) and Read/Write permissions for the data part (above the splitting address). The memory protection is effective on all access through the IRAMO and DRAMO buses. See details, see ESP-IDF api-reference Memory protection.
```

## 14.4.3 RTC FAST Memory

ESP32-C3's RTC FAST Memory is 8 KB. See the address of RTC FAST Memory below:

Table 14.4-8. RTC FAST Memory Address

| Memory   | Starting Address | Ending Address |
```