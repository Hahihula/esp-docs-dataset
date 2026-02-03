**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Body Text:**

via address fields (`I2C Base Address + Ox180`) ~(`I2C Base Address + Ox1FC`). Each byte in RX RAM occupies an entire word in the address space. Therefore, the address of the first byte is `I2C Base Address + 0x180`, the second byte is `I2C Base Address + 0x184`, and so on.

In FIFO mode, TX RAM of a master may wrap around to send data larger than 32 bytes. Set `I2C_FIFO_PRT_EN`. If the size of data to be sent is smaller than `I2C_TXFIFO_WM_THRHD` (master), an `I2C_TXFIFO_WM_INT` (master) interrupt is generated. After receiving the interrupt, software continues writing to `I2C_DATA_REG` (master). Please ensure that software writes to or refreshes TX RAM before the master sends data; otherwise it may result in unpredictable consequences.

In FIFO mode, RX RAM of a slave may also wrap around to receive data larger than 32 bytes. Set `I2C_FIFO_PRT_EN` and clear `I2C_RX_FULL_ACK_LEVEL`. If data already received (to be overwritten) is larger than `I2C_RXFIFO_WM_THRHD` (slave), an `I2C_RXFIFO_WM_INT` (slave) interrupt is generated. After receiving the interrupt, software continues reading from `I2C_DATA_REG` (slave).

**Subtitles and Sections:**

- **27.4.11 Data Conversion**
  DATA_Shifter is used for serial/parallel conversion, converting byte data in TX RAM to an outgoing serial bitstream or an incoming serial bitstream to byte data in RX RAM. `I2C_RX_FIRST` and `I2C_TX_LSB_FIRST` can be used to select LSB- or MSB-first storage and transmission of data.

- **27.4.12 Addressing Mode**
  Besides 7-bit addressing, the ESPI32-S3 I2C controller also supports 10-bit addressing and double addressing.
  
  - In a 10-bit addressing mode:
    Define the slave address as `SLV_ADDR`. In 7-bit addressing mode, the slave address is `SLV_ADDR[6:0];` in 10-bit addressing mode, the slave address is `SLV_ADDR[9:0]`.
    
    - **In 7-bit addressing mode**:
      The master only needs to send one byte of address, which comprises `SLV_ADDR[6:0]` and a `R/W` bit. In this case there are special cases called general call addressing (broadcast). It is enabled by setting `I2C_ADDR_BROADCAST_EN` in a slave. When the slave receives the general call address (`0x00`) from the master, it responds to all masters regardless of its own address.
    
    - **In 10-bit addressing mode**:
      The master needs two bytes of address: the first byte is `slave_addr_first_7bits` followed by a `R/W` bit and slave_addr_first_7bits should be configured as (`0x78 | SLV_ADDR[9:8]`). The second byte is `slave_addr_second_byte`, which can also include an 10-bit addressing mode. This configuration allows the master to enable or disable it by configuring `I2C_ADDR_10BIT_EN`.
      
      - `I2C_SLAVE_ADDR` should be configured as `SLV_ADDR[7:0]` and `I2C_SLAVE_ADDR[6:0]` can also include a 14-bit address. This configuration allows the master to enable or disable it by configuring `I2C_SLAVE_ADDR[14:7]`.
      
      - Since in this mode, there is one more byte than with an 8-bit addressing scheme (`byte_num` of the WRITE command and number of bytes in RAM increase).

**Additional Information:** 
When working in slave mode, I2C controller supports double addressing. The first address can be either a memory or register address; when using double addressing, RAM must also access non-FIFO mode.

**Footer:**
Espressif Systems  
995  
ESP32-S3 TRM (Version 1.7)  

**Navigation Links:** 
GoBack

**Action Button:**
Submit Documentation Feedback