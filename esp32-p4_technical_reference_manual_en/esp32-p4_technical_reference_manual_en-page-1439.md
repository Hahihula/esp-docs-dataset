
```markdown
- pseudo_inc: Equal to the value of AES_PSEUDO_INC, which configures the random incremental number of pseudo-rounds.

The total number of pseudo-rounds will be randomly in the range

[pseudo_base, pseudo_base + (2^pseudo_inc - 1)]

Random Number Update Frequency

AES_PSEUDO_RNG_CNT configures the frequency of random key updates in the pseudo-round function. The higher the configured value, the higher the update frequency. This value is usually recommended to be set to maximum (7).

25.9 Interrupts

ESP32-P4's AES can generate the following interrupt signal(s) that will be sent to the Interrupt Matrix:
- AES_INTR

There is one internal interrupt source from AES that can generate the above interrupt signal(s). The interrupt source from AES are listed with its trigger condition and the resulted interrupt signal(s) in Table 25.9-1.

Table 25.9-1. AES's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                     | Interrupt Signal |
|----------------------------|----------------------------------------|------------------|
| AES_DMA_DONE_INT           | Completion of an AES DMA operation     | AES_INTR         |

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.

25.10 Memory Summary

The addresses in this section are relative to the AES accelerator base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name        | Description | Size (byte) | Starting Address | Ending Address | Access |
|-------------|-------------|-------------|------------------|----------------|--------|
| AES_IV_MEM  | Memory IV   | 16 bytes    | 0x0050           | 0x005F         | R/W    |
| AES_H_MEM   | Memory H    | 16 bytes    | 0x0060           | 0x006F         | RO     |
| AES_JO_MEM  | Memory JO   | 16 bytes    | 0x0070           | 0x007F         | R/W    |
| AES_TO_MEM  | Memory TO   | 16 bytes    | 0x0080           | 0x008F         | RO     |
```