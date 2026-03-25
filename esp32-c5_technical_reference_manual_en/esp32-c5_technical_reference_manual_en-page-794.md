

```markdown
Chapter 18 Permission Control (PMS)

Register 18.113. LP_TEE_MO_MODE_CTRL_REG (0x0000)
```

```plaintext
31
+-------------------------------------------------------------+
| bit  | 3 | 2 | 1 | 0 |
|      +-----+-----+-----+-----+     Reset   |
|      | 0 0 0 0 ... 0 0 0 0 |         |
|      +---------------------+---------+
```

```markdown
LP_TEE_MO_MODE Configures the security mode for LP CPU.
O: TEE
1: REEO
2: REE1
3: REE2
(R/W)

LP_TEE_MO_LOCK Configures to lock the value of LP_TEE_MO_MODE.
O: Do not lock
1: Lock
(R/W)
```

```markdown
Register 18.114. LP_TEE_EFUSE_CTRL_REG (0x0004)
Register 18.115. LP_TEE_PMU_CTRL_REG (0x0008)
Register 18.116. LP_TEE_CLKRST_CTRL_REG (0x000C)
Register 18.117. LP_TEE_LP_AON_CTRL_CTRL_REG (0x0010)
Register 18.118. LP_TEE_LP_TIMER_CTRL_REG (0x0014)
Register 18.119. LP_TEE_LP_WDT_CTRL_REG (0x0018)
Register 18.120. LP_TEE_LP_PERI_CTRL_REG (0x001C)
Register 18.121. LP_TEE_LP_ANA_PERI_CTRL_REG (0x0020)
Register 18.122. LP_TEE_LP_IO_CTRL_REG (0x002C)
Register 18.123. LP_TEE_LP_TEE_CTRL_REG (0x0034)
Register 18.124. LP_TEE_UART_CTRL_REG (0x0038)
Register 18.125. LP_TEE_I2C_EXT_CTRL_REG (0x0040)
Register 18.126. LP_TEE_I2C_ANA_MST_CTRL_REG (0x0044)
Register 18.127. LP_TEE_LP_APM_CTRL_REG (0x004C)
```

```markdown
Espressif Systems

794

ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```