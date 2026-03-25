

# 30.6 Registers

The addresses in this section are relative to Random Number Generator base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 30.1. LPPERI_RNG_CFG_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31:0 | `reserved` |

- **LPPERI_RNG_SAMPLE_ENABLE** Configures whether to enable BUF_CHAIN.
  - 0: Disable
  - 1: Enable
  - (R/W)

- **LPPERI_RTC_TIMER_EN** Bit[0]: Configures whether to enable the RTC timer before CRC.
  - Bit[1]: Configures whether to enable the RTC timer after CRC.
  - 0: Disable
  - 1: Enable
  - (R/W)

## Register 30.2. LPPERI_RNG_DATA_SYNC_REG (0x0028)

| Bit | Description |
|-----|-------------|
| 31:0 | `reserved` |

- **LPPERI_RND_SYNC_DATA** Represents the RNG synchronization result.
  - (RO)