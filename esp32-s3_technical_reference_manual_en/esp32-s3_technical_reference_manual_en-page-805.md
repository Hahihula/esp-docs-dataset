**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Heading:**
Interrupt trigger.

**Body Text with Instructions and Details:**

- **See details below:**  
  - Configure Registers `WCL_CORE_m_MESSAGE_ADDR_REG` and `WCL CORE m MESSAGE_MAX_REG` to clear write_buffer, as described in Section 16.4.3.
  - Configure Registers `WCL CORE m ENTRY n ADDR REG (n: 1-13)` as the entry address of interrupts (or exceptions).
    - Note that all of ESP32-S3's interrupts and exceptions are using VecBase + offset as its address, therefore you need to configure `WCL CORE m ENTRY n ADDR REG (n: 1-13)` whenever you modify the VecBase.
  - Configure Register `WCL CORE m ENTRY_CHECK_REG` to enable the monitor of a certain entry. In this way, the CPU switches to the Secure World immediately when it executes the address monitored at this particular entry.

**List with Details about `Bit x controls the entry monitoring of Entry x (WCL CORE m ENTRY_x_ADDR_REG)`:**
- You can enable monitoring for more than one entry.
  - O: Disable monitoring
  - I: Enable monitoring

**Additional Information on Register Configuration:**  
Register `WCL CORE m ENTRY_CHECK_REG` is effective after configuration all the time till it's disabled, meaning you don't need to configure this register every time after each world switch.

**Subsection Title and Content:**
16.4.3 Clearing the write_buffer

ESP32-S3 has implemented `write_buffer`, which means the CPU buses can still hold some data from or execute instructions from the other world after world switches. To improve data security, we need to clear the writer_buffer before world switching:

- **Switching from Secure World to Non-secure World**
  - Use assembly instruction memw (memory wait).
  
- **Switching from Non-secure World to Secure World**
  - Switch CPU data bus:
    1. Pre-configure the following registers:
       * Configures Register `WCL CORE m MESSAGE_ADDR_REG` to an address in the Non-secure World;
       * Configure Register `WCL CORE m MESSAGE_MAX_REG` to Z (Z ∈ {3,4,...,16})
    2. Write sequences of 0, 1,..., Z-1, Z to the address configured in Register `WCL CORE m MESSAGE_ADDR_REG` before world switching.
       For example: if Z is configured to 3, then you need to write sequences of 0, 1, 2, 3 into the configured address; if Z is 5, then write 0, 1, 2, 3, 4, 5.

**Additional Information on CPU Switching:**
Afterwards, the CPU will switch its data bus to the other world once it detects the agreed sequences configured in `WCL CORE m MESSAGE_MAX_REG` are being written to the agreed address configured in `WCL CORE m MESSAGE_ADDR_REG`.

**Footer with Document Information and Feedback Link:**  
Espressif Systems  
805 ESP32-S3 TRM (Version 1.7)  
[Submit Documentation Feedback](#)