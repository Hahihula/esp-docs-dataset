

```markdown
## 1.9.5 Register Description

Register 1.33. pma_cfgX (0xBCO-0xBCF)

| Bit | Field        | Description                                                                 |
|-----|--------------|-----------------------------------------------------------------------------|
| 31  | A            | Configures address type. The functionality is the same as pmcfg register's A field. (R/W) <br> 0x0: OFF <br> 0x1: TOR <br> 0x2: NA4 <br> 0x3: NAPOT |
| 30  | LOCK         | Configures whether to lock the corresponding pma_cfgX and pma_addrX. (R/W) <br> 0: Not locked <br> 1: Locked. The write permission to the corresponding pma_cfgX and pma_addrX is revoked. It can only be unlocked by core reset. |
| 29  | reserved     |                                                                             |
| 28  | ATTRIBUTE    | Configures the values to be driven on DRAM attribute ports. (R/W)            |
| 27  |              |                                                                             |
| 24  |              |                                                                             |
| 5   | READ         | Configures read-permission for the corresponding region. <br> 0: Read not allowed <br> 1: Read allowed (R/W) |
| 4   | WRITE        | Configures write-permission for the corresponding region. <br> 0: Write not allowed <br> 1: Write allowed (R/W) |
| 3   | EXECUTE      | Configures execute-permission for the corresponding region. <br> 0: Execution not allowed <br> 1: Execution allowed (R/W) |
| 2   | TYPE         | Configures region type. (R/W) <br> 0x0: Invalid memory region (RWX access will be treated as 0, even if programmed to 1) <br> 0x1: Valid memory region (Programmed RWX access will be applicable) |
| 1   |              |                                                                             |
| 0   | Reset        | 0 0 0 0 0 0 0                                                               |
```