

```markdown
Chapter 28 SPI Controller (SPI)

Register 28.13. SPI_CLK_GATE_REG (0x00E8)
```

```text
(reserved)          (reserved)      (reserved)
                   SPI_CLK_EN
31 ────────────────────────────────────────────────────── 3   2   1   0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | 0 0 0
Reset
```

```markdown
SPI_CLK_EN Configures whether or not to enable clock gate. (R/W)

- 0: Disable
- 1: Enable
```

```text
Espressif Systems                      879                       ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```