

```markdown
Users can enable the pseudo-round function by setting AES_PSEUDO_EN to 1. The pseudo-round configuration is as follows.

Total number of pseudo-rounds

The total number of pseudo-rounds randomly inserted into an AES operation is controlled by the following register fields:

*   `pseudo_base`: Equal to the value of `AES_PSEUDO_BASE`, which configures the basic number of pseudo-rounds.
*   `pseudo_inc`: Equal to the value of `AES_PSEUDO_INC`, which configures the random incremental number of pseudo-rounds.

The total number of pseudo-rounds will randomly fall into the range:

[pseudo_base, pseudo_base + (2^pseudo_inc - 1)]

Random number update frequency

Users can set the frequency of random key updates in the pseudo-round function by configuring `AES_PSEUDO_RNG_CNT`. A higher value results in a higher update frequency. It is generally recommended to set this value to the maximum of 7.

19.8 Memory Summary

The addresses in this section are relative to the AES accelerator base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```

```markdown
| Name          | Description   | Size (byte) | Starting Address | Ending Address | Access |
|---------------|---------------|-------------|------------------|----------------|--------|
| AES_IV_MEM    | Memory IV     | 16 bytes    | 0x0050           | 0x005F         | R/W    |
```