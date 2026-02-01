**Title: Functional Description**

---

### 4.2.2.1 UART Controller (UART)

ESP32-P4 has six UART controllers, including five UARTs in the HP system and one low-power (LP) UART.

#### Feature List

Table 4-1. UART and LP UART Featvre Comparison

| UART Feature | LP UART Feature |
|--------------|-----------------|
| Programmable baud rate up to 5 Mbaud | 20 x 8-bit RAM, shared by the TX FIFO and RX FIFO of LP UART |
| 260 x 8-bit RAM, shared by TX FIFOs and RX FIFOs of the UART controllers | Full-duplex asynchronous communication |
| Data bits (5 to 8 bits) | Stop bits (1, 1.5, or 2 bits) |
| Parity bit | Special character AT_CMD detection |
| RS485 protocol | IrDA protocol |
| High-speed data communication using GDMA | Receive timeout |
| UART as wakeup source | Software and hardware flow control |

Three prescalable clock sources:
- XTAL_CLK
1. RC_FAST_CLK
2. XTAL_DIV_CLK
3. PLL_F80M_CLK

Pin Assignment:

For UARTO–UART4 interfaces, the pins used can be chosen from any GPIOs via the GPIO Matrix. By default, the pins connected to transmit and receive signals (UARTO_TXD_PAD and UARTO_RXD_PAD) of UARTO are multiplexed with GPIO37–GPIO38 and the eight-line interface of SPI2 controller via IO MUX.

For LP UART, the pins used can be chosen from any LP GPIOs via the LP GPIO Matrix. By default, the pins connected to transmit and receive signals (LP_UART_TXD_PAD and LP_UART_RXD_PAD) are multiplexed with LP_GPIO14–LP_GPIO15 via LP IO MUX.

---

### 4.2.2.2 SPI Controller (SPI)

The Serial Peripheral Interface (SPI) is a synchronous serial interface commonly used for communicating with external peripherals. The ESP32-P4 chip integrates four SPI controllers:

- MSPI controller, including two sub-controllers
  - FLASH MSPI controller

---

**Footer:**
Espressif Systems  
61  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)