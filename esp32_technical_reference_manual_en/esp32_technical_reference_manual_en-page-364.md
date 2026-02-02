**Chapter 20: SPI Controller (SPI)**

---

| Name | Description | SPI0 | SPI1 | SPI2 | SPI3 | Acc |
|------|-------------|------|------|------|------|-----|
| **SPI_USER_REG** | User defined command configuration | 3FF4301C | 3FF4201C | 3FF6401C | 3FF6501C | R/W |
| **SPI_USER1_REG** | Address and dummy cycle configuration | 3FF43020 | 3FF42020 | 3FF64020 | 3FF65020 | R/W |
| **SPI_USER2_REG** | Command length and value configuration | 3FF43024 | 3FF42024 | 3FF64024 | 3FF65024 | R/W |
| **SPI_MOSI_DLEN_REG** | MOSI length | 3FF43028 | 3FF42028 | 3FF64028 | 3FF65028 | R/W |
| **SPI_WO_REG** | SPI data register O | 3FF43080 | 3FF42080 | 3FF64080 | 3FF65080 | R/W |
| **SPI_W1_REG** | SPI data register 1 | 3FF43084 | 3FF42084 | 3FF64084 | 3FF65084 | R/W |
| **SPI_W2_REG** | SPI data register 2 | 3FF43088 | 3FF42088 | 3FF64088 | 3FF65088 | R/W |
| **SPI_W3_REG** | SPI data register 3 | 3FF4308C | 3FF4208C | 3FF6408C | 3FF6508C | R/W |
| **SPI_W4_REG** | SPI data register 4 | 3FF43090 | 3FF42090 | 3FF64090 | 3FF65090 | R/W |
| **SPI_W5_REG** | SPI data register 5 | 3FF43094 | 3FF42094 | 3FF64094 | 3FF65094 | R/W |
| **SPI_W6_REG** | SPI data register 6 | 3FF43098 | 3FF42098 | 3FF64098 | 3FF65098 | R/W |
| **SPI_W7_REG** | SPI data register 7 | 3FF4309C | 3FF4209C | 3FF6409C | 3FF6509C | R/W |
| **SPI_W8_REG** | SPI data register 8 | 3FF430A0 | 3FF420A0 | 3FF640A0 | 3FF650A0 | RO |
| **SPI_W9_REG** | SPI data register 9 | 3FF430A4 | 3FF420A4 | 3FF640A4 | 3FF650A4 | R/W |
| **SPI_W10_REG** | SPI data register 10 | 3FF430A8 | 3FF420A8 | 3FF640A8 | 3FF650A8 | RO |
| **SPI_W11_REG** | SPI data register 11 | 3FF430AC | 3FF420AC | 3FF640AC | 3FF650AC | R/W |
| **SPI_W12_REG** | SPI data register 12 | 3FF430B0 | 3FF420B0 | 3FF640B0 | 3FF650B0 | RO |
| **SPI_W13_REG** | SPI data register 13 | 3FF430B4 | 3FF420B4 | 3FF640B4 | 3FF650B4 | R/W |
| **SPI_W14_REG** | SPI data register 14 | 3FF430B8 | 3FF420B8 | 3FF640B8 | 3FF650B8 | RO |
| **SPI_W15_REG** | SPI data register 15 | 3FF430BC | 3FF420BC | 3FF640BC | 3FF650BC | R/W |

---

### DMA configuration registers

| Name | Description | SPI0 | SPI1 | SPI2 | SPI3 |
|------|-------------|------|------|------|------|
| **SPI_DMA_CONF_REG** | DMA register | 3FF43100 | 3FF42100 | 3FF64100 | 3FF65100 | R/W |
| **SPI_DMA_OUT_LINK_REG** | DMA outlink address and configuration | 3FF43104 | 3FF42104 | 3FF64104 | 3FF65104 | RO |
| **SPI_DMA_IN_LINK_REG** | DMA inlink address and configuration | 3FF43108 | 3FF42108 | 3FF64108 | 3FF65108 | R/W |
| **SPI_DMA_STATUS_REG** | DMA status | 3FF4310C | 3FF4210C | 3FF6410C | 3FF6510C | RO |
| **SPI_IN_ERR_EOFDES_ADDR_REG** | Descriptor address where an error occurs | 3FF43120 | 3FF42120 | 3FF64120 | 3FF65120 | R/W |
| **SPI_IN_SUC_EOFDES_ADDR_REG** | Descriptor address where EOF occurs | 3FF43124 | 3FF42124 | 3FF64124 | 3FF65124 | RO |
| **SPI_INLINK_DSCR_REG** | Current descriptor pointer | 3FF43128 | 3FF42128 | 3FF64128 | 3FF65128 | R/W |
| **SPI_INLINK_DSCR_BFO_REG** | Next descriptor data pointer | 3FF4312C | 3FF4212C | 3FF6412C | 3FF6512C | RO |
| **SPI_INLINK_DSCR_BF1_REG** | Current descriptor data pointer | 3FF43130 | 3FF42130 | 3FF64130 | 3FF65130 | R/W |

---

Espressif Systems  
364 ESP32 TRM (Version 5.6)  

Submit Documentation Feedback