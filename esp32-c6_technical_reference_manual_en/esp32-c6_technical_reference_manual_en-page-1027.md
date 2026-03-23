

```markdown
Chapter 31 Pulse Count Controller (PCNT)

Register 31.7. PCNT_INT_RAW_REG (0x0040)
```

![Diagram of PCNT_INT_RAW_REG register bit field layout with labels and reserved bits]

| Bit Field | Description |
|-----------|-------------|
| Reserved (bits 31:4) | (reserved) |
| Reset (bit 3:0) | Reset value for the raw interrupt status |

PCNT_CNT_THR_EVENT_Un_INT_RAW The raw interrupt status of the PCNT_CNT_THR_EVENT_Un_INT interrupt. (RO)

Register 31.8. PCNT_INT_ST_REG (0x0044)
```

![Diagram of PCNT_INT_ST_REG register bit field layout with labels and reserved bits]

| Bit Field | Description |
|-----------|-------------|
| Reserved (bits 31:4) | (reserved) |
| Reset (bit 3:0) | Reset value for the masked interrupt status |

PCNT_CNT_THR_EVENT_Un_INT_ST The masked interrupt status of the PCNT_CNT_THR_EVENT_Un_INT interrupt. (RO)

Register 31.9. PCNT_INT_ENA_REG (0x0048)
```

![Diagram of PCNT_INT_ENA_REG register bit field layout with labels and reserved bits]

| Bit Field | Description |
|-----------|-------------|
| Reserved (bits 31:4) | (reserved) |
| Reset (bit 3:0) | Reset value for the interrupt enable |

PCNT_CNT_THR_EVENT_Un_INT_ENA Write 1 to enable the PCNT_CNT_THR_EVENT_Un_INT interrupt. (R/W)
```