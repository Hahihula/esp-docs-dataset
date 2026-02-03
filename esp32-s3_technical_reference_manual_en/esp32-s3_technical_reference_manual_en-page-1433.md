**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Register Information Table Header:**
- Register Name
- Offset Range

**Table Content:**
- RMT_CHmSTATUS_REG (m = 4, 5, 6, 7) (0x0060, 0x0064, 0x0068, 0x006C)
  - Reserved
  - Reserved

**Field Descriptions:**
- **RMT_MEM_WADDR_EX_Chm**: This field records the memory address offset when receiver of channel m is using the RAM. (RO) APB bus.
- **RMT_APB_MEM_RADDR_Chm**: This field records the memory address offset when reads RAM over APB bus. (RO)
- **RMT_STATE_Chm**: This field records the FSM status of channel m. (RO)
- **RMT_MEM_OWNER_ERR_Chm**: This status bit will be set when the ownership of memory block is wrong. (RO)
- **RMT_MEM_FULL_Chm**: This status bit will be set if the receiver receives more data than the memory can fit. (RO)
- **RMT_APB_MEM_RD_ERR_Chm**: This status bit will be set if the offset address is out of memory size (overflows) when reads RAM via APB bus. (RO)

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback