

```markdown
Chapter 12 System Timer (SYSTIMER) GoBack

Register 12.1. SYSTIMER_CONF_REG (0x0000)

Continued from the previous page...

SYSTIMER_TIMER_UNIT1_WORK_EN Configures whether or not to enable UNIT1.
O: No effect
1: Enable
(R/W)

SYSTIMER_TIMER_UNITO_WORK_EN Configures whether or not to enable UNITO.
O: No effect
1: Enable
(R/W)

SYSTIMER_CLK_EN Configures register clock gating.
O: Only enable needed clock for register read or write operations
1: Register clock is always enabled for read and write operations
(R/W)

Register 12.2. SYSTIMER_UNITO_OP_REG (0x0004)

<table>
<thead>
<tr>
<th>Bit</th><th>31</th><th>30</th><th>29</th><th>28</th><th colspan="6"></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th>0</th>
</tr>
</thead>
<tbody>
<tr>
<td>Value</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>O</td><td>Reset</td>
</tr>
</tbody>
</table>

SYSTIMER_TIMER_UNITO_VALUE_VALID Represents UNITO value is synchronized and valid.
(R/SS/WTC)

SYSTIMER_TIMER_UNITO_UPDATE Configures whether or not to update timer UNITO,
i.e., reads the UNITO count value to SYSTIMER_TIMER_UNITO_VALUE_HI and SYS-
TIMER_TIMER_UNITO_VALUE_LO.
O: No effect
1: Update timer UNITO
(WT)
```