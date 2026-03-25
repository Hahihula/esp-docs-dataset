

```markdown
Figure 34.4-1. Acceptance Filter

message bit
acceptance code bit
XNOR acceptance mask bit
OR
AND
1 = accepted
0 = not accepted

• SFF
    – The entire 11-bit ID
    – RTR bit
    – Data byte 1 and Data byte 2

• EFF
    – The entire 29-bit ID
    – RTR bit

The following Figure 34.4-2 illustrates how the 32-bit code and mask values will be interpreted under Single Filter mode.

Figure 34.4-2. Single Filter Mode

ID = Identifier
DB = Data Byte
ACR = TWAI_ACCEPTANCE_CODE
AMR = TWAI_ACCEPTANCE_MASK

ACRO – Addr 0x0040 | ACR1 – Addr 0x0044 | ACR2 – Addr 0x0048 | ACR3 – Addr 0x004C
7 6 5 4 3 2 1 0   | 7 6 5 4 3 2 1 0   | 7 6 5 4 3 2 1 0   | 7 6 5 4 3 2 1 0

AMR0 – Addr 0x0050 | AMR1 – Addr 0x0054 | AMR2 – Addr 0x0058 | AMR3 – Addr 0x005C
7 6 5 4 3 2 1 0   | 7 6 5 4 3 2 1 0   | 7 6 5 4 3 2 1 0   | 7 6 5 4 3 2 1 0

EFF
ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21 ID.20 ID.19 ID.18 ID.17 ID.16 ID.15 ID.14 ID.13
ID.28 Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused

EFF
ID.28 ID.27 ID.26 ID.25 ID.24 ID.23 ID.22 ID.21 ID.20 ID.19 ID.18 ID.17 ID.16 ID.15 ID.14 ID.13
ID.28 Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused Unused

```

### 34.4.6.2 Dual Filter Mode

Dual Filter mode is enabled by clearing the `TWAI_RX_FILTER_MODE` bit to 0. This will cause the 32-bit code and mask values to define two separate filters referred to as filter 1 or filter 2. Under Dual Filter mode, a message will be accepted if it is accepted by one of the two filters.

The two filters can filter the following bits of data or remote frames:
```