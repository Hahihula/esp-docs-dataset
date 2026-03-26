

```markdown
| Frame Type | PM | PF | DAIF | PAM | DB | DA Filter Operation |
|:-----------|:----|:----|:------|:-----|:----|:-------------------------------------------------------------|
| Broadcast | 1   | X   | X     | X   | X  | Pass                                                                |
|           | 0   | X   | X     | X   | O  | Pass                                                                |
|           | O   | X   | X     | 1   |    | Fail                                                               |
| Unicast    | 1   | X   | X     | X   | X  | Pass all frames                                                     |
|            | O   | X   | O     | X   | X  | Pass on perfect/group filter match                               |
|            | O   | X   | 1     | X   | X  | Fail on perfect/group filter match                              |
|            | O   | 1   | X     | X   | X  | Pass on perfect/group filter match                              |
|            | O   | 1   | X     | X   | X  | Fail on perfect/group filter match                             |
|            | 1   | X   | X     | X   | X  | Pass all frames                                                   |
|            | X   | X   | X     | 1   | X  | Pass all frames                                                   |
|            | O   | X   | O     | O   | X  | Pass on perfect/group filter match and drop pause control frames if PCF = 0x. |
| Multicast  | O   | 1   | O     | O   | X  | Pass on perfect/group filter match and drop pause control frames if PCF = 0x. |
|            | O   | X   | 1     | O   | X  | Fail on perfect/group filter match and drop pause control frames if PCF = 0x. |
|            | O   | 1   | 1     | O   | X  | Fail on perfect/group filter match and drop pause control frames if PCF = 0x. |

The filtering parameters in the MAC Frame Filter Register described in Table 52.4-14 are as follows.

Parameter name
PM: Pass All Multicast
PF: Perfect Filter
DAIF: Destination Address Inverse Filtering
PAM: Pass All Multicast
DB: Disable Broadcast Frames

Parameter setting
1: Set
0: Cleared
X: Don't care
```