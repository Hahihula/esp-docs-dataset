

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Configuration registers**                |                                                                             |           |        |
| HINF_CFG_DATA0_REG                        | SDIO CIS configuration                                                      | 0x0000    | R/W    |
| HINF_CFG_DATA1_REG                         | SDIO configuration                                                          | 0x0004    | R/W    |
| HINF_CFG_DATA7_REG                         | SDIO configuration                                                          | 0x001C    | varies |
| HINF_CIS_CONF_Wn_REG(n: 0-7)               | SDIO CIS configuration                                                      | 0x0020+0x4*n | R/W   |
| HINF_CFG_DATA16_REG                        | SDIO CIS configuration                                                      | 0x0040    | R/W    |
| **Status registers**                       |                                                                             |           |        |
| HINF_CONF_STATUS_REG                       | SDIO CIS function 0 config0 status                                          | 0x0054    | RO     |

```