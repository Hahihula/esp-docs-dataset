

```markdown
- The first 16 bits of the 29-bit ID

The following Figure 31.4-3 illustrates how the 32-bit code and mask values will be interpreted in Dual Filter Mode.

Figure 31.4-3. Dual Filter Mode
```

```text
ID = Identifier                 ACR = TWAI_ACCEPTANCE_CODE
DB = Data Byte                  AMR = TWAI_ACCEPTANCE_MASK

Filter 1

ACR0 – Addr 0x0040
7 6 5 4 3 2 1 0

AMR0 – Addr 0x0050
7 6 5 4 3 2 1 0

SFF
ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21

EFF
ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21

Filter 2

ACR2 – Addr 0x0048
7 6 5 4 3 2 1 0

AMR2 – Addr 0x0058
7 6 5 4 3 2 1 0

SFF
ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21

EFF
ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21

ACR3 – Addr 0x004C
7 6 5 4 3 2 1 0

AMR3 – Addr 0x005C
7 6 5 4 3 2 1 0

DB1.3 DB1.2 DB1.1 DB1.0

ACR1– Addr 0x0044
7 6 5 4 3 2 1 0

AMR1 – Addr 0x0054
7 6 5 4 3 2 1 0

ID.19 ID.18 RTR DB1.7 DB1.6 DB1.5 DB1.4

ACR3 – Addr 0x004C
7 6 5 4 3 2 1 0

AMR3 – Addr 0x005C
7 6 5 4 3 2 1 0

DB1.3 DB1.2 DB1.1 DB1.0

ACR2 – Addr 0x0048
7 6 5 4 3 2 1 0

AMR2 – Addr 0x0058
7 6 5 4 3 2 1 0

ID.19 ID.18 RTR DB1.7 DB1.6 DB1.5 DB1.4
```

## 31.4.7 Error Management

The TWAI protocol requires that each TWAI node maintains the Transmit Error Counter (TEC) and Receive Error Counter (REC). The value of both error counters determines the current error state of the TWAI controller (i.e., Error Active, Error Passive, Bus-Off). The TWAI controller stores the TEC and REC values in `TWAI_TX_ERR_CNT_REG` and `TWAI_RX_ERR_CNT_REG` respectively, and they can be read by the CPU anytime. In addition to the error states, the TWAI controller also offers an Error Warning Limit (EWL) feature that can warn users of the occurrence of severe bus errors before the TWAI controller enters the Error Passive state.

The current error state of the TWAI controller is indicated via a combination of the following values and status bits: TEC, REC, `TWAI_ERR_ST`, and `TWAI_BUS_OFF_ST`. Certain changes to these values and bits will also trigger interrupts, thus allowing the users to be notified of error state transitions (see section 31.4.3). The following figure 31.4-4 shows the relation between the error states, values and bits, and error state related interrupts.
```