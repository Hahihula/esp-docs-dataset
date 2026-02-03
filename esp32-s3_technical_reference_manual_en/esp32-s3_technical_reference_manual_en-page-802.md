**Title: Chapter 16 World Controller (WCL)**

**Body Text:**
ESP32-S3’s CPU and slave devices are both configurable with permission to either Secure World and/or Non-Secure World:

- **CPU can be in either world at a particular time:**  
  - In Secure World: performs confidential operations;  
  - In Non-secure World: performs non-confidential operations;  
  - By default, CPU runs in Secure World after power-up, then can be programmed to switch between two worlds.

- All slave devices (including peripherals* and memories) can be configured to be accessible from the Secure World and/or the Non-secure World:
  - **Secure World Access:** this slave can be called from Secure World only, meaning it can be accessed only when CPU is in Secure World;
  - **Non-secure World Access:** this slave can be called from Non-secure World only, meaning it can be accessed only when CPU is in Non-secure World.

- Note that a slave can be configured to be accessible from both Secure World and Non-secure World simultaneously.  
For details, please refer to Chapter 15 Permission Control (PMS).

**Note:**
*World Controller itself is a peripheral, meaning it also can be granted with Secure World access and/or Non-secure World access, just like all other peripherals. However, to secure the world switch mechanism, World Controller should not be accessible from Non-secure world. Therefore, world controller **should not be granted with** Non-secure World access, preventing any modification to world controller from the Non-secure World.*

**Subtitle: When CPU accesses any slaves:**
1. First, CPU notifies the slave about its own world information;
2. Second, slave decides if it can be accessed by CPU based on the CPU’s worlds information and it's own world permission configuration.
   - If allowed, then this slave responds to CPU;
   - If not allowed, then this slave will not respond to CPU and trigger an interrupt.

In this way, the resources in the Secure World will not be illegally accessible by the Non-secure World in an unauthorized way. 

**Footer:**
Espressif Systems  
802 ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)