

```markdown
| Bit Field                                                                 | Description                                                                                                                                                  |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PMS_CORE_O_PIF_PMS_MONITOR_VIOLATE_INTR                                  | Stores the interrupt status of PIF bus unauthorized access. (RO)                                                                                              |
| PMS_CORE_O_PIF_PMS_MONITOR_VIOLATE_STATUS_HPORT_O                        | Stores the type of unauthorized access. 0: instruction. 1: data. (RO)                                                                                        |
| PMS_CORE_O_PIF_PMS_MONITOR_VIOLATE_STATUS_HSIZE                          | Stores the data type of unauthorized access. 0: byte. 1: half-word. 2: word. (RO)                                                                            |
| PMS_CORE_O_PIF_PMS_MONITOR_VIOLATE_STATUS_HWRITE                         | Stores the direction of unauthorized access. 0: read. 1: write. (RO)                                                                                          |
| PMS_CORE_O_PIF_PMS_MONITOR_VIOLATE_STATUS_HWORLD                         | Stores the privileged mode the CPU was in when the unauthorized access happened. <br> 01: privileged environment 10: unprivileged environment. (RO)               |

Register 14.67. PMS_CORE_O_PIF_PMS_MONITOR_2_REG (0x0138)
```