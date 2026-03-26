

```markdown
| Name | Description | Address | Access |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|:---------|:--------|
| DMA configuration and control registers |  |  |  |
| DMABUSMODE_REG | Bus mode register | 0x1000 | R/WS/SC |
| DMATXPOLLDEMAND_REG | Transmit poll demand register | 0x1004 | RO/WT |
| DMARXPOLLDEMAND_REG | Receive poll demand register | 0x1008 | RO/WT |
| DMARXBASEADDR_REG | Base address of the first receive descriptor | 0x100C | R/W |
| DMATXBASEADDR_REG | Base address of the first transmit descriptor | 0x1010 | R/W |
| DMASTATUS_REG | Base address of interrupt, error and other events | 0x1014 | R/SS/WC |
| DMAOPERATION_MODE_REG | Operation mode and command register | 0x1018 | R/SS/WC |
| DMAIN_EN_REG | Interrupt disable and enable register | 0x101C | R/W |
| DMAMISSEDFR_REG | Missed frame and buffer overflow counter register | 0x1020 | R/W |
| DMARINTWDTIMER_REG | Receive watchdog timer counter register | 0x1024 | R/W |
| DMAAHBSTATUS_REG | AHB master interface status register | 0x102C | RO |
| DMATXCURRDESC_REG | Current transmit descriptor register | 0x1048 | RO |
| DMARXCURRDESC_REG | Current receive descriptor register | 0x104C | RO |
| DMATXCURRADRR_BUF_REG | Current transmit buffer address register | 0x1050 | RO |
| DMARXCURRADRR_BUF_REG | Current receive buffer address register | 0x1054 | RO |
| MAC configuration and control registers |  |  |  |
| EMACCONFIG_REG | MAC configuration register | 0x0000 | R/W |
| EMACFF_REG | Frame filter register | 0x0004 | R/W |
| EMACMIADDR_REG | PHY access permission configuration register | 0x0010 | R/WS/SC |
| EMACMIIDATA_REG | PHY write and read data register | 0x0014 | R/W |
| EMACFC_REG | Frame flow control register | 0x0018 | varies |
| EMACVLANTAG_REG | 802.1Q VLAN tag register | 0x001C | R/W |
| EMACDEBUG_REG | Status and debug register | 0x0024 | RO |
| PMT_RWUFFR_REG | Wake-up frame filter register | 0x0028 | RO |
```