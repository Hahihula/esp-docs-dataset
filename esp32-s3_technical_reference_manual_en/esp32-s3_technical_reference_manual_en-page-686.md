**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Section Heading:**
15.3.2.2 Internal SRAMO Access Configuration

**Body Text:**
ESP32-S3’s Internal SRAMO includes Block0 and Block1 (see details in Table 15.3-3) and can be allocated to either CPU or ICACHE.

Note that once configured, the configuration applies for both CPU0 and CPU1.
ESP32-S3 uses the register described in Table 15.3-4 to allocate the SRAMO to either CPU or ICACHE:

**Table Title:**
Table 15.3-4. Internal SRAMO Usage Configuration

| Block | PMS_INTERNAL_SRAM USAGE _REG |
|-------|------------------------------|
| SRAM  | Block0                       | [0] |
|       | Block1                       | [1] |

A Set this bit to allocate a certain block to CPU. Clear this bit to allocate a certain block to ICACHE.
B For example, setting this bit indicates Block0 is allocated to CPU.

When a certain block is allocated to CPU, ESP32-S3 uses the registers listed in Table 15.3-5 to configure the instruction execution (X), write (W) and read (R) accesses of CPU’s IBUS, from the Secure World and Non-secure World, to this block:

**Table Title:**
Table 15.3-5. Access Configuration to Internal SRAMO

| Bus | From World | Configuration Registers | SRAMO | Access |
|-----|------------|--------------------------|-------|--------|
| IBUS | Secure World | PMS_CORE_X_IRAMO_PMSCONSTRAIN_2_REG [14:12] C [17:15] X/W/R |
|     | Non-secure World | PMS_CORE_X_IRAMO_PMSCONSTRAIN_1_REG [14:12] [17:15] X/W/R |

A To access the Internal SRAMO, CPU must be configured with both the usage permission and respective access permission.
B 1: with access; O: without access
C For example, configuring this field to Ob101 indicates CPU’s IBUS is granted with instruction execution and read accesses but not write access to SRAM Block0 from the Non-secure World.

**Section Heading:**
15.3.2.3 Internal SRAM1 Access Configuration

**Body Text:**
ESP32-S3’s Internal SRAM1 includes Block2 ~ Block8 (see details in Table 15.3-3) and can be:
- Accessed by CPU's DBUS, IBUS and GDMA at the same time
- Can be configured to be used as Trace memory
- Further split into up to 6 regions with independent access management for more flexible permission control.

ESP32-S3’s Internal SRAM1 can be further split into up to 6 regions with 5 split lines. Users can configure different access to each region independently.
To be more specific, the Internal SRAM1 can be first split into Instruction Region and Data Region by IRam0_DRam0_split_line:

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 
686 ESP32-S3 TRM (Version 1.7)