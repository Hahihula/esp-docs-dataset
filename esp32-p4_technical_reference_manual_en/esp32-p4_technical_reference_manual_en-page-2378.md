

```markdown
| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master)          | RESTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master)          | WRITE    | 0         | 0       | 1            | 1        |
| I2C_COMMAND2 (master)          | READ     | 0         | 0       | 1            | N-1       |
| I2C_COMMAND3 (master)          | READ     | 1         | 0       | 1            | 1        |
| I2C_COMMAND4 (master)          | STOP     | —         | —       | —            | —        |
```