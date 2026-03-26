

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.33. HP_SYSTEM_L2_MEM_INT_RECORDO_REG (0x00B0)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 25  |                                                                             |
| 24  |                                                                             |
| 22  |                                                                             |
| 21  |                                                                             |
| 20  |                                                                             |
|     | HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_MASTER                                    |
|     | HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_WE                                        |
|     | HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_ADDR                                      |

```
```markdown
0   0   0   0   0   0   0x0    0      0x0000 Reset

HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_ADDR Records the address when L2_MEM_EXCEED_ADDR_INT occurs. (RO)

HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_WE Records the operation (write/read) when L2_MEM_EXCEED_ADDR_INT occurs. (RO)

HP_SYSTEM_L2_MEM_EXCEED_ADDR_INT_MASTER Records source that triggered L2_MEM_EXCEED_ADDR_INT.
1: cachebus0
2: cachebus1
3: dma_axi
6: ahb
(RO)
```
```markdown
Espressif Systems

Submit Documentation Feedback

ESP32-P4 TRM
PRELIMINARY
```