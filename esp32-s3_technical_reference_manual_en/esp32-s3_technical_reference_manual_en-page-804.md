**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Number and Title:**
3.

**Body Text with Instructions for Register Configuration:**
Write any value to `Register WCL_CORE_m_World_UPDATE_REG`, indicating the configuration is done.
- Note:
  - `Register WCL\Core_m_World_UPDATE_REG` must be configured at last. 
  - Registers `WCL\Corem_WORLD_PERPARE_REG` and `WCL\Core_m_WorldTrigger_ADDR_REG` can be configured in any order.

After the configuration, you also need to use assembly instruction `memw` (memory wait) to clear write_buffer.
For details, see Section **16.4.3**.

**Body Text with Explanation:**
Afterwards, the World Controller keeps monitoring if CPU is executing the configured address of the application in Non-secure World. CPU switches to the Non-secure World once it executes the configured address, and executes the applications in the Non-secure World.
After configuration, the World Controller:
  - Keeps monitoring until the CPU executes the configured address and switches to the Non-secure World.

Write any value to `Register WCL\Core_m_World_Cancel_REG` to cancel the World Controller configuration. After the cancellation, CPU will not switch to the Non-secure World even it executes to the configured address. Note that you also need to use assembly instruction `memw` (memory wait) to clear write_buffer.
For details, see Section **16.4.3**.

The World Controller can only switch from Secure World to Non-secure World once per configuration. Therefore, the World Controller needs to be configured again after each world switch to prepare it for the next world switch.

**Subsection Title:**
16.4.2 From Non-secure World to Secure World

**Code Block with Explanation (Figure 16.4-2):**
```c
void main( void ) {
    ...
    Function B entry addr ENTRY_ADDR( X )
        ENTRY_CHECK=1<<X configuration
    ...
}
```

**Caption for Figure:**
Figure **16.4-2**: Switching From Non-secure World to Secure World

**Additional Information in Caption:**
CPU can only switch from Non-secure World to Secure World via `Interrupts` (or Exceptions). After configuring the World Controller, the CPU can switch back Non-secure World to Secure World upon the configured.

**Footer with Document Reference and Version Info:**
Espressif Systems
804 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback