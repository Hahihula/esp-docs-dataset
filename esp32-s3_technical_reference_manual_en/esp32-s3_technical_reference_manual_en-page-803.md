**Title:**
Chapter 16 World Controller (WCL)

**Subtitle:**
16.4 CPU’s World Switch

**Body Text:**
CPU can switch from Secure World to Non-secure World, and from Non-secure World to Secure World.

**Subsection Title:**
16.4.1 From Secure World to Non-secure World

**Code Block:**
```c
void main ( void ){
    ...
    WORLD_PREPARE=1<<1
    WORLD_TRIGGER_ADDR configuration
    WORLD_UPDATA
    ...
asm("memw");
    Entry Non-secure World
}
```

**Figure Caption and Description:**
Figure 16.4-1. Switching From Secure World to Non-secure World

ESP32-S3’s CPU only needs to complete the following steps to switch from Secure World to Non-secure World:

1. Configure the World Controller, as described below.
2. Clear the data stored in `write_buffer`, as described in Section 16.4.3.

After that, CPU can switch to the Non-secure World.

However, it’s worth noting that you cannot call the application in Non-secure world immediately after configuring the World Controller. For reasons such as CPU pre-indexed addressing and pipeline, it is possible that the CPU have already executed the application in Non-secure World before the World Controller configuration is effective, meaning the CPU runs unsecured application in the Secure World.

Therefore, you need to make sure the CPU only calls applications in the Non-secure world after the World Controller configuration takes effect. This can be guaranteed by declaring the applications in the Non-secure World as “noinline”.

**Subsection Title:**
Configuring the World Controller

The steps to configure the World Controller to switch the CPU from the Secure World to the Non-secure World are described below:

1. Write 0x2 to Register `WCL_CORE_m_WORLD_PERPARE_REG`, indicating the CPU needs to switch to the Non-secure World.
2. Configure Register `WCL_CORE_m_World_TRIGGER_ADDR_REG` as the entry address to the Non-secure World, i.e., the address of the application in the Non-secure World that needs to be executed.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version:**
803 ESP32-S3 TRM (Version 1.7)