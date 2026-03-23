

```markdown
Chapter 31 Pulse Count Controller (PCNT)

Register 31.10. PCNT_INT_CLR_REG (0x004C)
```

![Register bit field diagram for PCNT_INT_CLR_REG with labels and reset values](image_description: A horizontal register bit field labeled from bit 31 to bit 0, showing reserved bits followed by interrupt clear bits for U3, U2, U1, and U0. The rightmost four bits (bits 3-0) are labeled as PNT_CNT_THR_EVENT_U3_INT_CLR through PNT_CNT_THR_EVENT_U0_INT_CLR respectively. Bit positions beyond the first few reserved bits may be marked as "reserved".)

PCNT_CNT_THR_EVENT_Un_INT_CLR Write 1 to clear the PCNT_CNT_THR_EVENT_Un_INT interrupt. (WO)

Register 31.11. PCNT_DATE_REG (0x00FC)
```

![Register bit field diagram for PCNT_DATE_REG showing a single read-only value](image_description: A horizontal register labeled with "PCNT_DATE" diagonally across the top, containing one 32-bit field initialized to 0x19072601 at reset.)

PCNT_DATE Version control register. (R/W)
```