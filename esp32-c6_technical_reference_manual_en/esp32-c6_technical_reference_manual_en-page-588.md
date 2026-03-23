

```markdown
## 16.7.3 Low Power APMO Registers (LP_APMO_REG)

### Register 16.41. LP_APMO_REGION_FILTER_EN_REG (0x0000)

```
┌───────────────────────────────────────────────┬─────┬────┐
│                                            │  4  │  3 │
├───────────────────────────────────────────────┼─────┼────┤
│ 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 │    │ Ox1│ Reset
└───────────────────────────────────────────────┴─────┴────┘
```

**LP_APMO_REGION_FILTER_EN**: Configure bit `n` (0-3) to enable region `n`.

- 0: disable
- 1: enable

(R/W)

---

### Register 16.42. LP_APMO_REGIONn_ADDR_START_REG (n: 0-3) (0x0004+0xC*n)

```
┌───────────────────────────────────────┬────┐
│                                     │    │
├───────────────────────────────────────┼────┤
│                                        │ Reset
└───────────────────────────────────────┴────┘
```

**LP_APMO_REGIONn_ADDR_START**: Configures start address of region `n` (R/W)

---

### Register 16.43. LP_APMO_REGIONn_ADDR_END_REG (n: 0-3) (0x0008+0xC*n)

```
┌───────────────────────────────────────┬────┐
│                                     │    │
├───────────────────────────────────────┼────┤
│                                        │ Reset
└───────────────────────────────────────┴────┘
```

**LP_APMO_REGIONn_ADDR_END**: Configures end address of region `n` (R/W)
```