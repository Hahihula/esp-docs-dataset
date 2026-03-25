

```markdown
| Command registers of I2C_master | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:---------------------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMAND0 (master)           | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master)           | WRITE   | 0         | 0       | 1            | 2        |
| I2C_COMMAND2 (master)           | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND3 (master)           | WRITE   | 0         | 0       | 1            | 1        |
| I2C_COMMAND4 (master)           | READ    | 0         | 0       | 1            | N-1      |
| I2C_COMMAND5 (master)           | READ    | 1         | 0       | 1            | 1        |
| I2C_COMMAND6 (master)           | STOPT   | —         | —       | —            | —        |
```