

```markdown
## 16.9.4 HP_TEE_REG

The addresses in this section are relative to the TEE base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 16.53. TEE_Mn_MODE_CTRL_REG (n: 0-31) (0x0000+0x4*n)

| Bit 31 | ... | 2 | 1 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | Reset |

**TEE_Mn_MODE** Configures the security mode for master `n`.

- 0: TEE
- 1: REEO
- 2: REE1
- 3: REE2
(R/W)

**TEE_Mn_LOCK** Configures to lock the configuration of master `n`'s security mode.

- 0: Do not lock
- 1: Lock
(R/W)

### Register 16.54. TEE_CLOCK_GATE_REG (0x0080)

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | Reset |

**TEE_CLK_EN** Configures whether to keep the clock always on.

- 0: Enable automatic clock gating
- 1: Keep the clock always on
(R/W)
```