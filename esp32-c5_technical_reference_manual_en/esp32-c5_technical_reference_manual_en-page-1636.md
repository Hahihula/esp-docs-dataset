

```markdown
Chapter 42 Remote Control Peripheral (RMT)

Register 42.16. RMT_TX_SIM_REG (0x006C)
```
![Register 42.16 bit field diagram](image_description: A 32-bit register with bits labeled from left to right as [reserved] followed by RMT_TX_SIM_EN, RMT_TX_SIM_CH1, RMT_TX_SIM_CH0 at positions 3-0 respectively. Bit values are shown for reset state.)

```markdown
RMT_TX_SIM_CHn (n: 0-1) Configures whether to enable channel `n` to start sending data synchronously with other enabled channels.
O: No effect
1: Enable
(R/W)

RMT_TX_SIM_EN Configures whether to enable multiple of channels to start sending data synchronously.
O: No effect
1: Enable
(R/W)
```

```markdown
Register 42.17. RMT_CHm_RX_LIM_REG (m: 2-3) (0x0060+0x4*(m-2))
```
![Register 42.17 bit field diagram](image_description: A 32-bit register with bits labeled from left to right as [reserved] followed by RMT_RX_LIM_CHm at position 8, and a reset value of 0x80 shown.)

```markdown
RMT_RX_LIM_CHm Configures the maximum entries that Channel `m` can receive. (R/W)
```

```markdown
Register 42.18. RMT_DATE_REG (0x00CC)
```
![Register 42.18 bit field diagram](image_description: A 32-bit register with bits labeled from left to right as [reserved] followed by RMT_DATE at positions 27-28, and a reset value of 0x2108213 shown.)

```markdown
RMT_DATE Version control register. (R/W)
```

Espressif Systems

Submit Documentation Feedback

ESP32-C5 TRM (Version 1.0)

1636
```