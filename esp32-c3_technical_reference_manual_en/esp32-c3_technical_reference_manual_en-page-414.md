

```markdown
- In Secure World: performs confidential operations;
- In Non-secure World: performs non-confidential operations;
- By default, CPU runs in Secure World after power-up, then can be programmed to switch between two worlds.

• All slave devices (including peripherals* and memories) can be configured to be accessible from the Secure World and/or the Non-secure World:

  - Secure World Access: this slave can be called from Secure World only, meaning it can be accessed only when CPU is in Secure World;
  - Non-secure World Access: this slave can be called from Non-secure World only, meaning it can be accessed only when CPU is in Non-secure World.
    - Note that a slave can be configured to be accessible from both Secure World and Non-secure World simultaneously.

For details, please refer to Chapter 14 Permission Control (PMS).

Note:
* World Controller itself is a peripheral, meaning it also can be granted with Secure World access and/or Non-secure World access, just like all other peripherals. However, to secure the world switch mechanism, World Controller should not be accessible from Non-secure world. Therefore, world controller should not be granted with Non-secure World access, preventing any modification to world controller from the Non-secure World.

When CPU accesses any slaves:

1. First, CPU notifies the slave about its own world information;
2. Second, slave checks if it can be accessed by CPU based on the CPU’s world information and its own world permission configuration.
  - if allowed, then this slave responds to CPU;
  - if not allowed, then this slave will not respond to CPU and trigger an interrupt.

In this way, the resources in the Secure World will not be illegally accessible by the Non-secure World in an unauthorized way.

Note that the following CPU interrupt-related CSR registers can only be written to in the Secure World, and can only be read but not written to in the Non-secure World, thus ensuring that interrupts can only be controlled by the Secure World.

| Name                  | Description                      | Address | Access |
|-----------------------|----------------------------------|---------|--------|
| **Machine Trap Setup CSRs** |                                  |         |        |
| mstatus               | Machine Mode Status              | 0x300   | R/W    |
| mtvec                 | Machine Trap Vector              | 0x305   | R/W    |
| **Machine Trap Handling CSRs** |                              |         |        |
| mscratch             | Machine Scratch                  | 0x340   | R/W    |
| mepc                  | Machine Trap Program Counter     | 0x341   | R/W    |
| mcause                | Machine Trap Cause               | 0x342   | R/W    |
| mtval                 | Machine Trap Value               | 0x343   | R/W    |
```