

```markdown
| Name      | Description                          | Address | Access |
|-----------|--------------------------------------|---------|--------|
| tselect   | Trigger Select Register              | 0x7AO   | R/W    |
| tdata1    | Trigger Abstract Data 1              | 0x7A1   | R/W    |
| mcontrol   | tdata1 Shadow Register               | 0x7A1   | R/W    |
| tdata2    | Trigger Abstract Data 2              | 0x7A2   | R/W    |

## 4.5.3 Trigger Execution Flow

When a hart is halted and enters debug mode due to the firing of a trigger (action = 1):

* `dpc` is set to the current PC in the decoding phase
* The cause field in `dcsr` is set to 2, which means halt due to trigger

## 4.5.4 Register Summary

Below is a list of Trigger Module CSRs supported by the CPU. These are only accessible from machine mode.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```