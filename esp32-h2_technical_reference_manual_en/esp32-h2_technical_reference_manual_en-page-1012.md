
```markdown
| Bit 31-5 | Bit 4   | Bit 3   | Bit 2   | Bit 1   | Bit 0 |
|----------|---------|---------|---------|---------|-------|
| Reserved | BITNO.4¹| BITNO.3¹| BITNO.2¹| BITNO.1¹| BITNO.0¹|

Notes:
*   BITNO: Bit Number (BITNO) indicates the nth bit of a TWAI message where arbitration was lost.
```
```markdown
## 34.4.10 Transceiver Auto-Standby

It is common for TWAI transceivers to support a Standby mode to lower power consumption. TWAI transceivers will usually generate a standby signal that is asserted by the connected TWAI controller, thus allowing the controller to place the transceiver into standby when appropriate (e.g., when the bus will be idle for an extended period of time). Transceivers will exit Standby mode if the controller de-asserts the standby signal, or if the transceiver detects bus activity (also known as a wake-up feature).

ESP32-H2's TWAI controller supports both hardware control (i.e., automatic) and software control (i.e., manual) of the standby signal to control the switching of TWAI transceivers connected to the chip. When hardware controlled, the TWAI controller will automatically assert the standby signal when the bus remains idle for longer than a configurable amount of time. When software controlled, the standby signal can be manually asserted/de-asserted directly by the software.

*   **Hardware output:**
    1.  Set the `TWAI_HW_STANDBY_EN` field in the `TWAI_HW_CFG_REG` register to enable standby function for hardware.
    2.  Configure the `TWAI_HW_STANDBY_CNT_REG` register. This register indicates the time required before hardware triggers the standby signal after entering idle status, in which the value indicates the number of cycles of the TWAI controller operating clock (32 MHz by default).
*   **Software output:**
    1.  Set the `TWAI_SW_STANDBY_EN` field in the `TWAI_SW_STANDBY_CFG_REG` register to generate standby signals in the TWAI controller.

The standby signal generated using either of the above methods will be pulled down (cleared) when either of the following conditions is met:
1.  The standby signal will be automatically cleared when the TWAI controller exits the idle status.
2.  Users can also pull down the standby signal by setting the `TWAI_SW_STANDBY_CLR` field in the `TWAI_SW_STANDBY_CFG_REG` register.
```