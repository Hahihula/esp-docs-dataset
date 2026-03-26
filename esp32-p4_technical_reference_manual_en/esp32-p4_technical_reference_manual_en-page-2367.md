

```markdown
Address + 0x100, the second byte is I2C_Base_Address + 0x104, the third byte is I2C_Base_Address + 0x108,
and so on. The CPU can only read TX RAM via direct addresses. Bytes written to the TX RAM can be read
back by the CPU, via the direct addresses. Addresses for reading TX RAM are the same as addresses for
writing TX RAM.

RX RAM stores data the I2C controller receives during communication. When the I2C controller works in slave
mode, neither slave addresses sent by the master nor register addresses (only in dual address mode) will be
stored in RX RAM. Values of RX RAM can be read by software after I2C communication is completed.

RX RAM can only be read by the CPU. The CPU reads RX RAM either in FIFO mode or in non-FIFO mode (direct
address). In FIFO mode, the CPU reads RX RAM via the fixed address I2C_DATA_REG, with addresses for
reading RX RAM incremented automatically by hardware. In non-FIFO mode, the CPU accesses RX RAM directly
via address fields (I2C_Base_Address + 0x180) ~ (I2C_Base_Address + 0x1FC). Each byte in RX RAM occupies an
entire word in the address space. Therefore, the address of the first byte is I2C_Base_Address + 0x180, the
second byte is I2C_Base_Address + 0x184, the third byte is I2C_Base_Address + 0x188 and so on.

In FIFO mode, the TX RAM of a master may wrap around to send data larger than the FIFO depth. Set
I2C_FIFO_PRT_EN. If the size of data to be sent is smaller than I2C_TXFIFO_WM_THRHD (master), an
I2C_TXFIFO_WM_INT (master) interrupt is generated. After receiving the interrupt, the software continues
writing to I2C_DATA_REG (master). Please ensure that software writes to or refreshes TX RAM before the
master sends data, otherwise it may result in unpredictable consequences.

In FIFO mode, the RX RAM of a slave may also wrap around to receive data larger than the FIFO depth. Set
I2C_FIFO_PRT_EN and clear I2C_RX_FULL_ACK_LEVEL. If data already received (to be overwritten) is larger
than I2C_RXFIFO_WM_THRHD (slave), an I2C_RXFIFO_WM_INT (slave) interrupt is generated. After receiving
the interrupt, the software continues reading from I2C_DATA_REG (slave).

## 44.4.11 Data Conversion

DATA_Shifter is used for serial/parallel conversion, converting byte data in TX RAM to an outgoing serial
bitstream or an incoming serial bitstream to byte data in RX RAM. I2C_RX_LSB_FIRST and I2C_TX_LSB_FIRST
can be used to select LSB- or MSB-first storage and transmission of data.

## 44.4.12 Addressing Mode

The ESP32-P4 I2C controller supports 7-bit and 10-bit addressing. 10-bit addressing can be mixed with 7-bit
addressing. Besides, the ESP32-P4 I2C controller also supports dual address mode.

Define the slave address as SLV_ADDR. In 7-bit addressing mode, the slave address is SLV_ADDR[6:0]; in 10-bit
addressing mode, the slave address is SLV_ADDR[9:0].

In 7-bit addressing mode, the master only needs to send one byte of the address, which comprises
SLV_ADDR[6:0] and a R/W bit. In the 7-bit addressing mode, there is a special case called general call
addressing (broadcast). It is enabled by setting I2C_ADDR_BROADCASTING_EN in a slave. When the slave
receives the general call address (0x00) from the master and the R/W bit followed is 0, it responds to the
master regardless of its own address.

In 10-bit addressing mode, the master needs to send two bytes of address. The first byte is
slave_addr_first_7bits followed by a R/W bit, and slave_addr_first_7bits should be configured as (0x78 |
SLV_ADDR[9:8]). The second byte is slave_addr_second_byte, which should be configured as
SLV_ADDR[7:0].
```