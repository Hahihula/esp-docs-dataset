

```markdown
|Command registers|op_code|ack_value|ack_exp|ack_check_en|byte_num|
|:--------------------------|:--------|:----------|:-------|:------------|:---------|
|I2C_COMMANDO (master)|RSTART|—| | | |
|I2C_COMMAND1 (master)|WRITE|ack_value|ack_exp||N+1|
|I2C_COMMAND2 (master)|END|—| | |||
```

```markdown
|Command registers|op_code|ack_value|ack_exp|ack_check_en|byte_num|
|:--------------------------|:--------|:----------|:-------|:------------|:---------|
|I2C_COMMANDO (master)|WRITE|ack_value|ack_exp||M|
|I2C_COMMAND1 (master)|END/STOP|—| | |||
```
```