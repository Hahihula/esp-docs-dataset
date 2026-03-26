
```markdown
| I2C_COMMAND2 (master) | RSTART | — | — | — | — |
|------------------------|--------|----|----|----|----|
| I2C_COMMAND3 (master) | mWRITE | 0 | 0 | 1 | 1 |
| I2C_COMMAND4 (master) | READ   | 0 | 0 | 1 | N-1 |
| I2C_COMMAND5 (master) | READ   | 1 | 0 | 1 | 1 |
| I2C_COMMAND6 (master) | STOP   | — | — | — | — |
```