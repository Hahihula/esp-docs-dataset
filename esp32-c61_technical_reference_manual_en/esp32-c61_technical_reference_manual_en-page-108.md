

```markdown
| Name       | Description                          | Address | Access |
|------------|--------------------------------------|---------|--------|
| tselect    | Trigger select register              | 0x7A0   | R/W    |
| tdata1     | Trigger abstract data 1              | 0x7A1   | R/W    |
| tdata2     | Trigger abstract data 2              | 0x7A2   | R/W    |
| tdata3     | Trigger abstract data 3              | 0x7A3   | R/W    |
| tinfo      | Trigger information                  | 0x7A4   | RO     |
| tcontrol   | Global trigger control               | 0x7A5   | R/W    |
| mcontext   | Trigger context                      | 0x7A8   | R/W    |

### 1.10.2.6 Register Description

#### Register 1.98. tselect (0x7A0)

tselect Configures the index (0-3) of the selected trigger unit. (R/W)

```
┌─────────────────────────────┬───────┐
│ 30                        │ 2     │
├─────────────────────────────┼───────┤
│ 0x00000000                 │ 0x0   │ Reset
└─────────────────────────────┴───────┘
```

#### Register 1.99. tdata1 (0x7A1)

```
┌────────────────────────────┬────────┐
│ type    dmode              │ data   │
├────────────────────────────┼────────┤
│ 31      28                  │        │
│ 0x2     0                   │        │
└────────────────────────────┴────────┘
```

**type** Represents the trigger type. This field is reserved since only match type (0x2) triggers are supported. (RO)

**dmode** This is set to 1 if a trigger is being used by the debugger.
- 0: Both Debug and M mode can write the tdata1 and tdata2 registers at the selected tselect.
- 1: Only Debug Mode can write the tdata1 and tdata2 registers at the selected tselect. Writes from other modes are ignored.
Note: Only writable from debug mode. (R/W)

**data** Configures the abstract tdata1 content. This will always be interpreted as fields of `mcontrol` since only match type (0x2) triggers are supported. (R/W)
```