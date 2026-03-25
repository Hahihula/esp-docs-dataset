

```markdown
- SFF
  - The entire 11-bit ID
  - RTR bit
  - Data byte 1 (for filter 1 only)
- EFF
  - The first 16 bits of the 29-bit ID
```

The following Figure 34.4-3 illustrates how the 32-bit code and mask values will be interpreted in Dual Filter mode.

Figure 34.4-3. Dual Filter Mode

## 34.4.7 Error Management

The TWAI protocol requires that each TWAI node maintains the Transmit Error Counter (TEC) and Receive Error Counter (REC). The value of both error counters determines the current error state of the TWAI controller (i.e., Error Active, Error Passive, Bus-Off). The TWAI controller stores the TEC and REC values in `TWAI_TX_ERR_CNT_REG` and `TWAI_RX_ERR_CNT_REG` respectively, and they can be read by the CPU anytime. In addition to the error states, the TWAI controller also offers an Error Warning Limit (EWL) feature that can warn users of the occurrence of severe bus errors before the TWAI controller enters the Error Passive state.
```