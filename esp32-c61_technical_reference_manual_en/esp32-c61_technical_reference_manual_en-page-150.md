

```markdown
Register 2.13. TRACE_FILTER_COMPARATOR_CONTROL_REG (0x0030)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  |                                | (reserved)                                                                  |
| 29  |                                | (reserved)                                                                  |
| 28  |                                | (reserved)                                                                  |
| 27  | TRACE_MATCH_MODE               |                                                                             |
| 26  | (reserved)                     |                                                                             |
| 25  | TRACE_S_NOTIFY                 |                                                                             |
| 24  | (reserved)                     |                                                                             |
| 23  | TRACE_S_FUNCTION               |                                                                             |
| 22  | (reserved)                     |                                                                             |
| 21  | TRACE_S_INPUT                  |                                                                             |
| 20  | (reserved)                     |                                                                             |
| 19  | TRACE_P_NOTIFY                 |                                                                             |
| 18  | (reserved)                     |                                                                             |
| 17  | TRACE_P_FUNCTION               |                                                                             |
| 16  | (reserved)                     |                                                                             |
| 15  |                                |                                                                             |
| 14  |                                |                                                                             |
| 13  |                                |                                                                             |
| 12  |                                |                                                                             |
| 11  |                                |                                                                             |
| 10  |                                |                                                                             |
| 9   |                                |                                                                             |
| 8   |                                |                                                                             |
| 7   |                                |                                                                             |
| 6   |                                |                                                                             |
| 5   |                                |                                                                             |
| 4   |                                |                                                                             |
| 3   |                                |                                                                             |
| 2   |                                |                                                                             |
| 1   |                                |                                                                             |
| 0   | Reset                          |                                                                             |

TRACE_P_INPUT Configures the input of the primary comparator for matching.
O: iaddr
1: tval
(R/W)

TRACE_P_FUNCTION Configures the function for the primary comparator.
O: Equal
1: Not equal
2: Less than
3: Less than or equal
4: Greater than
5: Greater than or equal
Others: Always match
(R/W)

TRACE_P_NOTIFY Configures whether to explicitly report an instruction address matched against the primary comparator.
O: Not report
1: Report
(R/W)

TRACE_S_INPUT Configures the input of the secondary comparator for matching.
O: iaddr
1: tval
(R/W)

TRACE_S_FUNCTION Configures the function of for secondary comparator.
O: Equal
1: Not equal
2: Less than
3: Less than or equal
4: Greater than
5: Greater than or equal
6: The second comparator value is the masked value of the primary comparator
Others: Always match
(R/W)

Continued on the next page...
```