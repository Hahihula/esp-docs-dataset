
```markdown
Chapter 18 Permission Control (PMS)                                                                 GoBack


Register 18.42. LP_APM_INT_EN_REG (0x00E8)

[Diagram: Register bitfield with labels]
(reserved)
LP_APM_M1_APM_INT_EN
LP_APM_MO_APM_INT_EN

31 | ... | 2 | 1 | 0
+----+------------------+-----+---+---+
|    |                |     |   | Reset |
+----+------------------+-----+---+---+

LP_APM_MO_APM_INT_EN Configures to enable LP_APM_CTRL MO interrupt.
O: Disable
1: Enable
(R/W)

LP_APM_M1_APM_INT_EN Configures to enable LP_APM_CTRL M1 interrupt.
O: Disable
1: Enable
(R/W)


Register 18.43. LP_APM_CLOCK_GATE_REG (0x00EC)

[Diagram: Register bitfield with labels]
(reserved)
LP_APM_CLK_EN

31 | ... | 1 | 0
+----+------------------+-----+---+
|    |                |     | Reset |
+----+------------------+-----+---+

LP_APM_CLK_EN Configures whether to keep the clock always on.
O: Enable automatic clock gating
1: Keep the clock always on
(R/W)


Register 18.44. LP_APM_DATE_REG (0x00FC)

[Diagram: Register bitfield with labels]
(reserved)
LP_APM_DATE

31 | 28 | 27 | ... | 0
+----+----+-----+-----+
|    |    |     | Reset |
+----+----+-----+-----+

LP_APM_DATE Version control register. (R/W)

Espressif Systems                                                                                                                                              777
ESP32-C5 TRM (Version 1.0)
```