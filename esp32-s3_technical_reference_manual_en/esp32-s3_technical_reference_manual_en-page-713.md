**Title:**
Chapter 15 Permission Control (PMS)

**Header:**
Register 15.4. PMS_INTERNAL_SRAM USAGE_1_REG (0x0014)

**Diagram Description with Labels and Values:**
- The diagram shows a register layout for the specified address.
- It includes labels such as "PMS_INTERNAL_SRAM_CPU_USAGE", "PMS_INTERNAL_SRAM_DCACHE_USAGE", etc., each associated with specific bits in the register.

**Body Text (Descriptions of Register Fields):**

1. **PMS_INTERNAL_SRAM_ICACHE USAGE**
   - Configures certain blocks of SRAM0 are allocated for CPU or ICACHE.
   - Access: Read/Write

2. **PMS_INTERNAL_SRAM_DCACHE USAGE**
   - Configures certain blocks of SRAM2 are allocated for CPU or DCACHE.
   - Access: Read/Write

3. **PMS_INTERNAL_SRAM_CPU USAGE**
   - Configures this field to allow CPU to use certain blocks of SRAM1.
   - Access: Read/Write

**Footer Information (Document Identification):**

- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack