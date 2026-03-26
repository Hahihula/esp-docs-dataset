

```markdown
## 1.10.2.5 Register Description

Register 1.118. pma_cfg[n] (n: 0-15) (0xBC0+0x1*n)

| A | LOCK | reserved | ATTRIBUTE | ... | READ | WRITE | EXECUTE | reserved | TYPE |
|---|------|----------|-----------|-----|------|-------|---------|----------|------|
| 31| 30   | 29       | 28        | 27  | 24   | 23    | ...     | ...      | ...  |
|   |      |          |           |     | 2    | 0     |         |          | Reset|

A Configures address type. The functionality is the same as pmcfg register's A field.
- 0x0: OFF
- 0x1: TOR
- 0x2: NA4
- 0x3: NAPOT (R/W)

LOCK Configures whether to lock the corresponding pma_cfgX and pma_addrX.
- 0: Not lock
- 1: Lock. The write permission to the corresponding pma_cfgX and pma_addrX is revoked. It can only be unlocked by core reset. (R/W)

ATTRIBUTE Configures the values to be driven on DRAM attribute ports.

Bit 27:
- 0: Cacheable
- 1: Non-cacheable

Bit 26:
- 0: Write-back
- 1: Write-through

Bit 25:
- 0: Write miss allocate
- 1: Write miss no allocate

Bit 24:
- 0: Read miss allocate
- 1: Read miss no allocate (R/W)

READ Configures read-permission for the corresponding region.
- 0: Read not allowed
- 1: Read allowed (R/W)

Continued on the next page...
```