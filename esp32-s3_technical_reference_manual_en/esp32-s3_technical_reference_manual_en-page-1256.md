**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Subtitle:**
33.6 Registers

**Body Text:**

The addresses in this section are relative to USB Serial/JTAG Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection Title:**
Register 33.1. USB_SERIAL_JTAG_EP1_REG (0x0000)

**Table Description for Register 33.1:**

| Bit | Name                          |
|-----|-------------------------------|
| 8   |                             |
| ... |                             |
| 7   |                             |
| 6   |                             |
| 5   |                             |
| 4   |                             |
| 3   |                             |
| 2   |                             |
| 1   |                             |
| 0   |                             |

**Description:**
USB_SERIAL_JTAG_RDWR_BYTE
Write and read byte data to/from UART Tx/Rx FIFO through this field. When USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT is set, then user can write data (up to 64 bytes) into UART Tx FIFO. When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is set, user can check USB_SERIAL_JTAG_OUT_EP1_WR_ADDR USB_SERIAL_JTAG_OUT_EP1_RD_ADDR to know how many data is received, then read data from UART Rx FIFO.

**Subsection Title:**
Register 33.2. USB_SERIAL_JTAG_EP1_CONF_REG (0x0004)

**Table Description for Register 33.2:**

| Bit | Name                          |
|-----|-------------------------------|
| 8   |                             |
| ... |                             |
| 7   |                             |
| 6   |                             |
| 5   |                             |
| 4   |                             |
| 3   |                             |
| 2   |                             |
| 1   |                             |
| 0   |                             |

**Description:**
USB_SERIAL_JTAG_WR_DONE
Set this bit to indicate writing byte data to UART Tx FIFO is done.

**Bit Description for USB_SERIAL_JTAG_WR_DONE (WT):**

- **1**: Indicate UART Tx FIFO is not full and can write data into in. After writing USB_SERIAL_JTAG_WR_DONE, this bit would be 1'b0 until data in UART Tx FIFO is read by USB Host.
- **0**: 

**Bit Description for USB_SERIAL_JTAG_IN_EP_DATA_FREE (1'b1):**

- **1**: Indicate there is data in UART Rx FIFO.

**Bit Description for USB_SERIAL_JTAG_OUT_EP_DATA_AVAIL (1'b1):**

- **1**: Indicate there is data in UART Rx FIFO. 

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback