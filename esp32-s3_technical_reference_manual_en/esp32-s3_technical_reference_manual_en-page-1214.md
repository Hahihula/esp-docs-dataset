**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Heading:**
31.7 Registers

**Body Text with Annotations and Descriptions of Register Bits:**

- **Register Description:** Here means separate line.
- The left describes the access in Operation Mode, while on the right belongs to Reset Mode marked by red color.

The addresses mentioned are relative to Two-wire Automotive Interface base address provided in Table 4.3-3 from Chapter 4 System and Memory.

**Register Name:**
Register 31.1 TWAI_MODE_REG (0x0000)

**Bit Description with Binary Representation, Functionality, and Access Mode Indication:**  
- **TWAI_RESET_MODE**: This bit is used to configure the operation mode of the TWAI Controller.
  - Reset mode; O: Operation mode
  - R/W access
  
- **TWAI_LISTEN_ONLY_MODE**: 
  - Value = 1 (Listen only mode)
  - In this mode, nodes will receive messages from bus without generating acknowledge signal nor updating RX error counter.  
  - Access Mode is Read/Write

- **TWAI_SELF_TEST_MODE**:
  - Value = 1
  - Self test mode.
  - TX nodes can perform successful transmission without receiving the acknowledge signal in this mode, often used to test a single node with self reception request command (R/W)
  
- **TWAI_RX_FILTER_MODE**: 
  - This bit is for configuring filter mode. O: Dual filter mode; R: Single filter mode
  - Access Mode can be Read/Write

**Register Name and Description:** Register 31.2 TWAI_BUS_TIMING_O_REG (0x018)

- **TWAI_BAUD_PRESC**: Baud Rate Prescaler value, determines the frequency dividing ratio.
  - R/W access
  
- **TWAI_SYNC_JUMP_WIDTH**: Synchronization Jump Width (SJW), ranging from position Tq to width. 
  - Access Mode is Read/Write

**Footer:**
Espressif Systems
1214 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback