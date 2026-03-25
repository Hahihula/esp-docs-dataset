

```markdown
| maddress(31-0) | Start Address       | Size (bytes) |
|----------------|---------------------|--------------|
| aaa...aaaaaaaaa0 | aaa...aaaaaaaaaa0  | 2            |
| aaa...aaaaaaaaa1 | aaa...aaaaaaaaaa00 | 4            |
| aaa...aaaaaaaaa11 | aaa...aaaaaaaaaa000 | 8            |
| aaa...aaaaaaaaa111 | aaa...aaaaaaaaaa0000 | 16           |
| ...            | ...                 |              |
| a01...11111111   | a00...0000000000    | 2^31         |

## 1.11.3 Trigger Execution Flow

When hart is halted and enters debug mode due to the firing of a trigger (action = 1):
- `dpc` is set to current PC (in decode stage)
- cause field in `dcscr` is set to 2, which means halt due to trigger
- `hit` bit is set to 1, corresponding to the trigger(s) which fired

When hart goes into trap due to the firing of a trigger (action = 0):
- `mepc` is set to current PC (in decode stage)
- `mcause` is set to 3, which means breakpoint exception
- `mpre` is set to the value in `mte` right before trap
- `mte` is set to 0
- `hit` bit is set to 1, corresponding to the trigger(s) which fired

Note: If two different triggers fire at the same time, one with action = 0 and another with action = 1, then hart is halted and enters debug mode.

## 1.11.4 Register Summary

Below is a list of Trigger Module CSRs supported by the CPU. These are only accessible from machine mode.
```