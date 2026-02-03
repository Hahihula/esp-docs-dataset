**Title: Appendix A**

---

### Table of Contents

- **A.3. Ethernet_MAC**
  
- **A.4. IO_MUX**

---

#### Section Title (A.3): Ethernet_MAC

##### Subtitle and Description:
Table 6-3.

| Pin Name | Function6 | MII (int_osc) | MII (ext_osc) | RMII (int_osc) | RMII (ext_osc) |
|----------|-----------|---------------|---------------|----------------|----------------|
| GPIO0    | EMAC_TX_CLK | TX_CLK(I)     | TX_CLK(I)     | CLK_OUT(O)     | EXT_OSC_CLK(I) |
| GPIO5    | EMAC_RX_CLK | RX_CLK(I)     | RX_CLK(I)     | —              | —              |
| GPIO21   | EMAC_TX_EN  | TX_EN(O)      | TX_EN(O)      | TX_EN(O)       | TX_EN(O)       |
| GPIO19   | EMAC_TXD0   | TXD[0](O)     | TXD[0](O)     | TXD[0](O)      | TXD[0](O)      |
| GPIO22   | EMAC_TXD1   | TXD[1](O)     | TXD[1](O)     | TXD[1](O)      | TXD[1](O)      |
| MTMS     |            |               |               |                |                |
| MTDI     |            | TXD[2](O)     | TXD[2](O)     | —              | —              |
| MTCK     | EMAC_TXD3  | TXD[3](O)     | TXD[3](O)     | —              | —              |
| MTCK     |            | RX_ER(I)      | RX_ER(I)      |                |                |
| GPIO27   | EMAC_RX_DV | RX_DV(I)      | RX_DV(I)      | CRS_DV(I)      | CRS_DV(I)      |
| GPIO25   | EMAC_RXD0  | RXD[0](I)     | RXD[0](O)     | RXD[0](O)      | RXD[0](O)      |
| GPIO26   | EMAC_RXD1  | RXD[1](I)     | RXD[1](O)     | RXD[1](O)      | RXD[1](O)      |
| UOTXD    | EMAC_RXD2  | RXD[2](I)     | RXD[2](I)     | —              | —              |
| MTDO     | EMAC_RXD3  | RXD[3](I)     | RXD[3](O)     | —              | —              |
| GPIO16   | EMAC_CLK_OUT | CLK_OUT(O)    | —             | CLK_OUT(O)     | —              |
| GPIO17   | EMAC_CLK_OUT_180 | CLK_OUT_180(O) | —            | CLK_OUT_180(O) | —              |
| GPIO4    | EMAC_TX_ER  | TX_ERR(O)*    | TX_ERR(O)*    | MDC(O)         | MDC(O)         |
| In GPIO Matrix* | —           | MDC(O)        | MDIO(IO)       | MDIO(IO)       | MDIO(IO)       |
| In GPIO Matrix* | —           | CRS(I)         | CRS(I)         |                |                |
| In GPIO Matrix* | —           | COL(I)         | COL(I)         |                |                |

**Notes:**
1. The GPIO Matrix can be any GPIO.
2. The TX_ERR(O) is optional.

---

#### Section Title (A.4): IO_MUX

For the list of IO_MUX pins, please see the next page.

---

**Footer Information:**  
Espressif Systems  
ESP32 Series Datasheet v5.2  
Submit Documentation Feedback  

Page 69