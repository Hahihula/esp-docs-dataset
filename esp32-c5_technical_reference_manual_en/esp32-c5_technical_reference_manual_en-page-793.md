

```markdown
Register 18.110. TEE_BUS_ERR_CONF_REG (0x0FF0)

31 | [reserved] | TEE_BUS_ERR_RESP_EN
---------------------------------------------------------------|-------------|--------------------
0   | 0         | 0                 | Reset

TEE_BUS_ERR_RESP_EN Configures whether to return error message to CPU when access is blocked.
O: Disable
1: Enable
(R/W)


Register 18.111. TEE_CLOCK_GATE_REG (0x0FF8)

31 | [reserved] | TEE_CLK_EN
---------------------------------------------------------------|-------------|--------------------
0   | 0         | 0                 | Reset

TEE_CLK_EN Configures whether to keep the clock always on.
O: Enable automatic clock gating
1: Keep the clock always on
(R/W)


Register 18.112. TEE_DATE_REG (0x0FFC)

31   28    27
---------------------------------------------------------------|-------------|--------------------
0    | 0      | 0                 | Ox2406200         | Reset

TEE_DATE Version control register. (R/W)


18.9.6 LP_TEE_REG

The addresses in this section are relative to the LP_TEE base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```