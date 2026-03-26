

```markdown
Register 1.118. pma_cfgn (n: 0-15) (0xBCO+0x1*n)

Continued from the previous page...

WRITE Configures write-permission for the corresponding region.
    0: Write not allowed
    1: Write allowed
        (R/W)

EXECUTE Configures execute-permission for the corresponding region.
    0: Execution not allowed
    1: Execution allowed
        (R/W)

TYPE Configures region type.
    0x0: Invalid memory region (RWX access will be treated as 0, even if programmed to 1)
    0x1: Valid memory region (Programmed RWX access will be applicable)
        (R/W)

Register 1.119. pma_addrn (n: 0-15) (0xBDO+0x1*n)

ADDR Configures address. The functionality is same as pmpaddr register. (R/W)
```