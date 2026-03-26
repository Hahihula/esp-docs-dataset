

```markdown
Chapter 53 Two-Wire Automotive Interface (TWAI)

The following Figure 53.4-3 illustrates how the 32-bit code and mask values will be interpreted in Dual-filter mode.

ID = Identifier
DB = Data Byte
ACR = TWAI_ACCEPTANCE_CODE
AMR = TWAI_ACCEPTANCE_MASK

Filter 1

SFF
EFF

ACR0 – Addr 0x0040
7 6 5 4 3 2 1 0

ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21

AMR0 – Addr 0x0050
7 6 5 4 3 2 1 0

ACR1 – Addr 0x0044
7 6 5 4 3 2 1 0

ID.19 ID.18 ID.17 ID.16 ID.15 ID.14 ID.13

AMR1 – Addr 0x0054
7 6 5 4 3 2 1 0

ACR3 – Addr 0x004C
7 6 5 4 3 2 1 0

ID.8 ID.9 ID.10 ID.11 ID.12

AMR3 – Addr 0x005C
7 6 5 4 3 2 1 0

Filter 2

ACR2 – Addr 0x0048
7 6 5 4 3 2 1 0

ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21

AMR2 – Addr 0x0058
7 6 5 4 3 2 1 0

ACR3 – Addr 0x004C
7 6 5 4 3 2 1 0

ID.19 ID.18 ID.17 ID.16 ID.15 ID.14 ID.13

AMR3 – Addr 0x005C
7 6 5 4 3 2 1 0

Figure 53.4-3. Dual-Filter Mode


53.4.6 Error Management

The TWAI protocol requires that each TWAI node maintains the Transmit Error Counter (TEC) and Receive Error Counter (REC). The value of both error counters determines the current error state of the TWAI controller (i.e., Error Active, Error Passive, Bus-Off). The TWAI controller stores the TEC and REC values in TWAI_TX_ERR_CNT_REG and TWAI_RX_ERR_CNT_REG respectively, and they can be read by the CPU anytime. In addition to the error states, the TWAI controller also offers an Error Warning Limit (EWL) feature that can warn users of the occurrence of severe bus errors before the TWAI controller enters the Error Passive state.

The current error state of the TWAI controller is indicated via a combination of the following values and status bits: TEC, REC, TWAI_STATUS_ERR, and TWAI_STATUS_NODE_BUS_OFF. Certain changes to these values and bits will also trigger interrupts, so that users are notified of error state transitions (see section 53.5). The following figure 53.4-4 shows the relation between the error states, values and bits, and error state related interrupts.
```