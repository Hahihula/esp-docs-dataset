

```markdown
| maddress(31-0) | Start Address       | Size (bytes) |
|----------------|---------------------|--------------|
| aaa........aaaaaaa0O | aaa.......aaaaaaa0O | 2            |
| aaa........aaaaaaa01 | aaa.......aaaaaaa00 | 4            |
| aaa........aaaaaaa011 | aaa.......aaaaaaa00O | 8            |
| aaa........aaaaaaa0111 | aaa.......aaaaaaa000O | 16           |
| ...            |                     |              |
| aaaa...0111111111   | aaa.......aaa0000000O | 2^8          |

### Table 2.10-4. NAPOT encoding for maddress

#### 2.10.2.4 Trigger Execution Flow

When hart is halted and enters debug mode due to the firing of a trigger (action = 1):
*   dpc is set to current PC (in decode stage)
*   cause field in dcsr is set to 2, which means halt due to trigger
*   hit bit is set to 1, corresponding to the trigger(s) which fired

When a hart goes into a trap due to the firing of a trigger (action = 0):
*   mepc is set to current PC (in decode stage)
*   mcause is set to 3, which means breakpoint exception
*   mpte is set to the value in mte right before trap
*   mte is set to 0
*   hit bit is set to 1, corresponding to the trigger(s) which fired

Note: If two different triggers fire at the same time, one with action = 0 and another with action = 1, the hart is halted and enters debug mode.

#### 2.10.2.5 Register Summary

Below is a list of Trigger Module CSRs supported by the CPU. These are only accessible from machine mode.
```