

```markdown
Register 20.15. HP_SYSTEM_HP_CACHE_CLK_CONFIG_REG (0x0020)

31 | 6 | 5 | 4 | 3 | 2 | 1 | 0
--+---+---+---+---+---+---+---+
0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 0 | 1 | 1
                                                Reset

HP_SYSTEM_L2_CACHE_CLK_ON Configures whether or not to enable L2 cache clock.
O: Disable
1: Enable
(R/W)

HP_SYSTEM_L1_D_CACHE_CLK_ON Configures whether or not to enable L1 dcache clock.
O: Disable
1: Enable
(R/W)

HP_SYSTEM_L1_I_CACHE_CLK_ON Configures whether or not to enable L1 ichache 1 clock.
O: Disable
1: Enable
(R/W)

HP_SYSTEM_L1_IO_CACHE_CLK_ON Configures whether or not to enable L1 ichache O clock.
O: Disable
1: Enable
(R/W)
```