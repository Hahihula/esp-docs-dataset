

```markdown
Chapter 48 Pulse Count Controller (PCNT)

Register 48.7. PCNT_INT_RAW_REG (0x0040)
```

![Register Diagram: PCNT_INT_RAW_REG](diagram of register with bits labeled and reserved fields noted)

| Bit Field | Description |
|-----------|-------------|
| `reserved` | Reserved bits, not used for configuration or status reading. |
| `PCNT_CNT_THR_EVENT_U3_INT_RAW` | Raw interrupt status bit for threshold event U3. (RO) |
| `PCNT_CNT_THR_EVENT_U2_INT_RAW` | Raw interrupt status bit for threshold event U2. (RO) |
| `PCNT_CNT_THR_EVENT_U1_INT_RAW` | Raw interrupt status bit for threshold event U1. (RO) |
| `PCNT_CNT_THR_EVENT_U0_INT_RAW` | Raw interrupt status bit for threshold event U0. (RO) |

```markdown
PCNT_CNT_THR_EVENT_Un_INT_RAW The raw interrupt status of the PCNT_CNT_THR_EVENT_Un_INT interrupt. (RO)
```

Register 48.8. PCNT_INT_ST_REG (0x0044)

![Register Diagram: PCNT_INT_ST_REG](diagram of register with bits labeled and reserved fields noted)

| Bit Field | Description |
|-----------|-------------|
| `reserved` | Reserved bits, not used for configuration or status reading. |
| `PCNT_CNT_THR_EVENT_U3_INT_ST` | Masked interrupt status bit for threshold event U3. (RO) |
| `PCNT_CNT_THR_EVENT_U2_INT_ST` | Masked interrupt status bit for threshold event U2. (RO) |
| `PCNT_CNT_THR_EVENT_U1_INT_ST` | Masked interrupt status bit for threshold event U1. (RO) |
| `PCNT_CNT_THR_EVENT_U0_INT_ST` | Masked interrupt status bit for threshold event U0. (RO) |

```markdown
PCNT_CNT_THR_EVENT_Un_INT_ST The masked interrupt status of the PCNT_CNT_THR_EVENT_Un_INT interrupt. (RO)
```

Register 48.9. PCNT_INT_ENA_REG (0x0048)

![Register Diagram: PCNT_INT_ENA_REG](diagram of register with bits labeled and reserved fields noted)

| Bit Field | Description |
|-----------|-------------|
| `reserved` | Reserved bits, not used for configuration or status reading. |
| `PCNT_CNT_THR_EVENT_U3_INT_ENA` | Interrupt enable bit for threshold event U3. (R/W) |
| `PCNT_CNT_THR_EVENT_U2_INT_ENA` | Interrupt enable bit for threshold event U2. (R/W) |
| `PCNT_CNT_THR_EVENT_U1_INT_ENA` | Interrupt enable bit for threshold event U1. (R/W) |
| `PCNT_CNT_THR_EVENT_U0_INT_ENA` | Interrupt enable bit for threshold event U0. (R/W) |

```markdown
PCNT_CNT_THR_EVENT_Un_INT_ENA Write 1 to enable the PCNT_CNT_THR_EVENT_Un_INT interrupt. (R/W)
```

Espressif Systems

2533

ESP32-P4 TRM

PRELIMINARY

Submit Documentation Feedback
```