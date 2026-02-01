**4 Functional Description**

- **4.1.4.12 System Registers**
  The System Registers in the ESP32-P4 chip are used to configure various auxiliary chip features.

  - Feature List:
    - Control External memory encryption and decryption
    - Control HP core/LP core debugging
    - Control Bus timeout protection

- **4.1.4.13 Debug Assistant**
  The Debug Assistant provides a set of functions to help locate bugs and issues during software debugging. It offers various monitoring capabilities and logging features to assist in identifying and resolving software errors efficiently.

  - Feature List:
    - Read/write monitoring: Monitors whether the High-Performance dual-core CPU (HP CPU0 and HP CPU1) bus reads from or writes to a specified memory address space. A detected read or write in the monitored address space will trigger an interrupt.
    - Stack pointer (SP) monitoring: Monitors whether the SP exceeds the specified address space. A bounds violation will trigger an interrupt.
    - Program counter (PC) logging: Records the PC value. The developer can get the last PC value at the most recent reset of HP CPU0 or HP CPU1.
    - Bus access logging: Recorders the information about bus access. When the HP CPU0, HP CPU1, or the Direct Memory Access controller (DMA) writes a specified value, the Debug Assistant module will record the data type, address of this write operation, and additionally the PC value when the write is performed by HP CPU0 or HP CPU1, and push such information to the HP L2MEM.

- **4.1.4.14 LP Mailbox**
  ESP32-P4 integrates an LP Mailbox module which provides an efficient inter-core communication mechanism between the LP CPU and HP CPU0/1. The LP Mailbox module comprises of sixteen 32-bit message registers that the LP CPU and HP CPUO/1 can use to store and exchange messages. Inter-core communication between LP CPU and HP CPUO/1 is achieved through an interrupt mechanism implemented within the LP Mailbox module.

  - Feature List:
    - Sixteen 32-bit message registers for inter-core communication
    - LP CPU external interrupt signal
    - HP CPU0/1 external interrupt signal

**Espressif Systems**
50 ESP32-P4 Series Datasheet v0.6  
[Submit Documentation Feedback](#)