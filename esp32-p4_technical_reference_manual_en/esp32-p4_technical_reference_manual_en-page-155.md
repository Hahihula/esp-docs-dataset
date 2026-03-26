

```markdown
| maddress(31-0) | Start Address       | Size (bytes) |
|----------------|---------------------|--------------|
| aaa...aaaaaaaaa0 | aaa...aaaaaaaaaa0  | 2            |
| aaa...aaaaaaaaa1 | aaa...aaaaaaaaaa00 | 4            |
| aaa...aaaaaaaaa11 | aaa...aaaaaaaaaa000 | 8            |
| aaa...aaaaaaaaa111 | aaa...aaaaaaaaaa0000 | 16           |
| ...            | ...                 | ...          |
| aaa...01111111   | aaa...aaa000000    | 2^8          |

tcontrol CSR is common to all trigger units. It is used for preventing triggers from causing repeated exceptions in machine mode while execution is happening inside a trap handler. This also disables breakpoint exceptions inside ISRs by default, although, it is possible to manually enable this right before entering an ISR, for debugging purposes. This CSR is not relevant if a trigger is configured to enter debug mode.

### 1.11.3.4 Trigger Execution Flow

When hart is halted and enters debug mode due to the firing of a trigger (action = 1):
*   dpc is set to current PC (in decode stage)
*   cause field in dcsr is set to 2, which means halt due to trigger
*   hit bit is set to 1, corresponding to the trigger(s) which fired

When hart goes into trap due to the firing of a trigger (action = 0):
*   mepc is set to current PC (in decode stage)
*   mcause is set to 3, which means breakpoint exception
*   mpte is set to the value in mte right before trap
*   mte is set to 0
*   hit bit is set to 1, corresponding to the trigger(s) which fired

Note: If two different triggers fire at the same time, one with action = 0 and another with action = 1, then hart is halted and enters debug mode.

### 1.11.3.5 Register Summary

Below is a list of Trigger Module CSRs supported by the CPU. These are only accessible from machine mode.
```