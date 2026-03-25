

```markdown
| Name                                       | Description                          | Address   | Access |
|--------------------------------------------|--------------------------------------|-----------|--------|
| PAU_REGDMA_CLK_CONF_REG                   | Clock control register              | 0x0004    | R/W    |
| PAU_REGDMA_ETM_CTRL_REG                   | ETM start configuration/control register | 0x0008   | varies |
| PAU_REGDMA_LINK_O_ADDR_REG                | Link address configuration register O | 0x000C   | varies |
| PAU_REGDMA_LINK_1_ADDR_REG                | Link address configuration register 1 | 0x0010   | varies |
| PAU_REGDMA_LINK_2_ADDR_REG                | Link address configuration register 2 | 0x001C   | varies |
| PAU_REGDMA_LINK_3_ADDR_REG                | Link address configuration register 3 | 0x0018   | varies |
| PAU_REGDMA_LINK_MAC_ADDR_REG              | Link MAC address register           | 0x000C    | varies |
| PAU_REGDMA_CURRENT_LINK_ADDR_REG          | Current link address register       | 0x0020    | varies |
| PAU_REGDMA_BACKUP_ADDR_REG                | Backup address register             | 0x0024    | varies |
| PAU_REGDMA_MEM_ADDR_REG                   | Memory address configuration register | 0x0028   | RO     |
| PAU_REGDMA_BKP_CONF_REG                   | Link configuration register         | 0x002C    | R/W    |
| PAU_INT_ENA_REG                           | Interrupt register                  | 0x0030    | R/W    |
| PAU_INT_RAW_REG                           | Interrupt register                  | 0x0034    | R/WTC/SS|
| PAU_INT_CLR_REG                           | Interrupt register                  | 0x0038    | WT     |
| PAU_INT_ST_REG                            | Interrupt register                  | 0x003C    | RO     |

Version Register
----------------

PAU_DATE_REG                               | Version control register            | 0x03FC    | R/W    |
```