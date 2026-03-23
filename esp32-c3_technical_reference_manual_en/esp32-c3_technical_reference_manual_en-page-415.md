

```markdown
Chapter 15 World Controller (WCL)
GoBack

15.4 CPU's World Switch

CPU can switch from Secure World to Non-secure World, and from Non-secure World to Secure World.

15.4.1 From Secure World to Non-secure World

void main(void){
    ...
    ...
    WORLD_PREPARE=1<<1
    WORLD_TRIGGER_ADDR
    WORLD_UPDATE
    Configuration
    Function A Entry addr ←
    asm("fence")
    Function A → Entry Non-secure World
}

Figure 15.4-1. Switching From Secure World to Non-secure World

ESP32-C3's CPU only needs to complete the following steps to switch from Secure World to Non-secure World:

1. Write 0x2 to Register WCL_CORE_O_WORLD_PERPARE_REG, indicating the CPU needs to switch to the Non-secure World.
2. Configure Register WCL_CORE_O_World_TRIGGER_ADDR_REG as the entry address to the Non-secure World, i.e., the address of the application in the Non-secure World that needs to be executed.
3. Write any value to Register WCL_CORE_O_World_UPDATE_REG, indicating the configuration is done.

Note:
• Registers WCL_COREm_WORLD_PERPARE_REG and WCL_CORE_O_World_TRIGGER_ADDR_REG can be configured in any order. Register WCL_CORE_O_World_UPDATE_REG must be configured at last.

Afterwards, the World Controller keeps monitoring if CPU is executing the configured address of the application in Non-secure World. CPU switches to the Non-secure World once it executes the configured address, and executes the applications in the Non-secure World.

After configuration, the World Controller:
• Keeps monitoring until the CPU executes the configured address and switches to the Non-secure World.
  – Write any value to Register WCL_CORE_O_World_Cancel_REG to cancel the World Controller configuration. After the cancellation, CPU will not switch to the Non-secure World even it executes to the configured address.
• The World Controller can only switch from the Secure World to Non-secure World once per configuration. Therefore, the World Controller needs to be configured again after each world switch to
```