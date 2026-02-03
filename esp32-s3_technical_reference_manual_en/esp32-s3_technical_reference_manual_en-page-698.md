**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Table Titles and Content:**

- **Table 15.5-3. Split the External SRAM into Four Split Regions for GDMA**
  - Columns:
    - "Split Regions"
    - "Starting Address (included)"
    - "Ending Address (not included)"
  - Rows:
    - Region0, Starting Address = `0x3C000000`, Ending Address not specified
    - Region1^4, Starting Address = `PMS_EDMA_BOUNDARY_0_REG`^1, Ending Address not specified
    - Region2^4, Starting Address = `PMS_EDMABOUNDARY_1_REG`^1, Ending Address not specified
    - Region3^3, Starting Address = `PMS_EDMABOUNDARY_2_REG`^1, Ending Address = `0x3E000000`

- **Table 15.5-4. Access Configuration of External SRAM via GDMA**
  - Columns:
    - "Peripherals"
    - "Access Configuration" (Region1)
    - "Access Configuration" (Region2)
    - "Access"
  - Rows include various peripherals like SPI2, SPI3, UHCIO, I2S0, Camera-LCD Controller with corresponding access configurations and attributes.

**Text Content:**
- Explanation of the configuration process for accessing external SRAM via GDMA.
- Note that some regions cannot be accessed by peripherals due to security reasons (e.g., Region 1).
- Users can configure peripherals' access through specific registers using GDMA commands like `PMS_EDMA_PMS_SPI2 ATTR1`.

**Section Title:**
15.6 Unauthorized Access and Interrupts

**Body Text under Section:**
Any attempt to access ESP32-S3’s slave device without configured permission is considered an unauthorized access.

- This will be handled as described below:
  - Attempted actions with default values, in particular:

**Footer Information:**
- Document version information at the bottom of each page.