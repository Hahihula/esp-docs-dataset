

```markdown
Chapter 27 Digital Signature Algorithm (DSA) GoBack

## 27.5 Register Summary

The addresses in this section are relative to Digital Signature Algorithm base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                        | Description                                                                 | Address | Access |
|-----------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Control/Status registers** |                                                                             |         |        |
| DS_SET_START_REG            | Activates the DSA module                                                    | 0x0E00  | WT     |
| DS_SET_CONTINUE_REG         | Continues DSA operation                                                     | 0x0E04  | WT     |
| DS_SET_FINISH_REG           | Ends DSA operation                                                           | 0x0E08  | WT     |
| DS_QUERY_BUSY_REG           | Status of the DSA module                                                    | 0x0E0C  | RO     |
| DS_QUERY_KEY_WRONG_REG      | Checks the reason why DS_KEY is not ready                                   | 0x0E10  | RO     |
| DS_QUERY_CHECK_REG          | Queries DSA check result                                                     | 0x0E14  | RO     |
| **Configuration registers** |                                                                             |         |        |
| DS_KEY_SOURCE_REG           | Configures DSA key source                                                   | 0x0E18  | R/W    |
| version control register    | Version control register                                                    | 0x0E20  | R/W    |
```