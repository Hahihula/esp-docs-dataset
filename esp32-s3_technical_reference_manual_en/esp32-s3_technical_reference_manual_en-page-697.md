**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Body Text with List and Table:**

- SRAM can be split into 4 regions, the length of each should be the integral multiples of 64 KB.
- Also, the starting address of each region should also be aligned to 64 KB.

The following registers can be used to configure how the flash or SRAM are split:

**Table Title:**
Table 15.5-1. Split the External Memory into Split Regions

| Split Regions | Starting Address^1 | Length^2 |
|---------------|--------------------|----------|
| Flash Region (n: 0~3) | SYSCON_FLASH_ACE_n_ADDR_REG | SYSCON_FLASH_ACE_n_SIZE_REG |
| SRAM Region (n: 0~3) | SYSCON_SRAM_ACE_n_ADDR_REG | SYSCON_SRAM_ACE_n_SIZE_REG |

1 Configuring this field with the actual address, which should be aligned to 64 KB.
2 When configuring the length of Region n, note the total length of all flash or SRAM regions should be less than 1 GB, respectively.

3 Each region cannot overlap with others.

**Subsection Title:**
15.5.2 Access Configuration

Each split regions for flash and SRAM can be configured with different permission independently via Registers SYSCON_SRAM_ACE_n ATTRB and SYSCON_FLASH_ACE_n ATTRB.

**Table Title:**
Table 15.5-2. Access Configuration of External Memory Regions

| Split Regions | Configuration Registers | Access Configuration | CACHE | SPI^1 |
|---------------|--------------------------|----------------------|-------|-------|
| Flash Region (n: 0~3) | SYSCON_FLASH_ACE_n ATTRB | [2:0] | [5:3] | [7:6]^C D |
| SRAM Region n (n: 0~3) | SYSCON_SRAM_ACE_n ATTRB REG | [2:0] | [5:3] | [7:6] |

A These bits are configured in order W/R/X
B These bits are configured in order W/R

C For example, configuring this field to 0b010 indicates CACHE is granted with the read access but not the write or instruction execution accesses from the Secure WORLD to the Flash Region n.

D For example, configuring this field to 0b01 indicates SPI is granted with the read access but not the write access to the Flash Region n.

**Subsection Title:**
15.5.3 GDMA

ESP32-S3’s 32 MB External SRAM can be independently split into four regions, of which the Region1 and Region2 are accessible to GDMA.

**Footer Information:**
Espressif Systems
697 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback