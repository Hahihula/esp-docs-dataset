

```markdown
Register 3.13. TRACE_FILTER_COMPARATOR_CONTROL_REG (0x0030)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 31  |                                | (reserved)                                                                  |
| 29-18| TRACE_MATCH_MODE              | (reserved)                                                                  |
| 17  | TRACE_S_NOTIFY                | (reserved)                                                                  |
| 16  | TRACE_P_NOTIFY                | (reserved)                                                                  |
| 15  | TRACE_S_FUNCTION              | (reserved)                                                                  |
| 14  | TRACE_P_FUNCTION              | (reserved)                                                                  |
| 13  |                                | (reserved)                                                                  |
| 12  |                                | (reserved)                                                                  |
| 11  |                                | (reserved)                                                                  |
| 10  |                                | (reserved)                                                                  |
| 9   |                                | (reserved)                                                                  |
| 8   |                                | (reserved)                                                                  |
| 7   | TRACE_S_INPUT                 | (reserved)                                                                  |
| 6   | TRACE_P_INPUT                 | (reserved)                                                                  |
| 5   |                                | (reserved)                                                                  |
| 4   |                                | (reserved)                                                                  |
| 3   |                                | (reserved)                                                                  |
| 2   |                                | (reserved)                                                                  |
| 1   |                                | (reserved)                                                                  |
| 0   | Reset                         | 0                                                                             |

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