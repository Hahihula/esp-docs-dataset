

```markdown
## 1.9.5 Register Description

Register 1.33. pma_cfgX (0xBC0-0xBCF)

| A | Lock | reserved | Attribute | reserved | Access | reserved | Type |
|---:|:-----:|:---------:|:----------:|:---------:|:-------:|:---------:|:------|
| 31 | 30   | 29        | 28         | 27        | 24      | 6         | 5     | 2    | 1    | 0    |
| 2  | 0    | 0         | 0          |           |         |           |       |      |      | Reset|

A Configures address type. The functionality is the same as pmcfg register's A field.
- 0x0: OFF
- 0x1: TOR
- 0x2: NA4
- 0x3: NAPOT (R/W)

Lock Configures whether to lock the corresponding pma_cfgX and pma_addrX.
- 0: Not lock
- 1: Lock. The write permission to the corresponding pma_cfgX and pma_addrX is revoked. It can only be unlocked by core reset. (R/W)

Attribute Configures the values to be driven on DRAM attribute ports. (R/W)

Type Configures region type.
- 0x0: Invalid memory region (RWX access will be treated as 0, even if programmed to 1)
- 0x1: Valid memory region (Programmed RWX access will be applicable) (R/W)

Register 1.34. pma_addrX (0xBDO-0xBDF)

| Addr |
|------|
| 31   | 0    |
|      | Reset|

Addr Configures address. The functionality is same as pmpaddr register. (R/W)
```