**Related Documentation and Resources**

### Access Types for Registers

Sections **Register Summary** and **Register Description** in TRM chapters specify access types for registers and their fields.

Most frequently used access types and their combinations are as follows:

- RO: Read only. User application can read from this register/field; usually combined with other access types.
- WO: Write Only. User application can write to this register/field, usually combined with other access types.
- WT: Write Once. User application can write to this register/field once (only allowed to write 1); writing O is invalid.

**Access Types List**
- RO
- R/W
- RW1
- WL
- WO
- WT
- RF
- RS
- RC
- WF
- WS

#### Access Type Descriptions:
- **R**: Read. User application can read from this register/field; usually combined with other access types.
- **RO**: Read only. User application can only read from this register/field.

**HRO (Hardware Read Only)**: Only hardware can read from this register/field, used for storing default settings or variable parameters in registers.

- **W**: Write. User application can write to this register/field; usually combined with other access types.
- **WO**: Write only. User application can only write to this register/field field (only allowed to write 1).

**SS (Self Set)**: On a specified event, hardware automatically writes 1s to the register/field.

- **SC**: Self clear. On a specified event, hardware automatically writes O's to this register/field.
- **SM**: Self modify. On a specified event, hardware automatically writes value(s) from this register/field (used with multi-bit fields).

**SU (Self Update)**: On a specified event, hardware updates the field.

- **RS**: Read-to-set. If user application reads data to/from this register/field.
- **RC**: Read-to-clear. If user application clears or writes O's from/to this register/field; used with multi-bit fields in registers.

**RF (Read From FIFO)**: If a new value is written by the hardware, it automatically updates and stores that information into the register/field via APB bus.
- **WF**: Write to FIFO. User application can write data directly onto the FIFO buffer without affecting other parts of memory or system state; used with multi-bit fields.

**WS (Write Any Value)**: If user writes any value, it is automatically stored in this field and updated accordingly by hardware mechanisms such as DMA transfers etc., which may include setting up interrupts based on specific conditions met during operation. 

---

Espressif Systems  
1520  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)