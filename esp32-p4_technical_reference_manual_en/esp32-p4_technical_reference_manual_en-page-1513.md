

# 30.5 Register Summary

The addresses in this section are relative to the RSA Digital Signature Peripheral (RSA_DS) base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers** | | | |
| DSA_IV_O_REG | IV block data | 0x0630 | WO |
| DSA_IV_1_REG | IV block data | 0x0634 | WO |
| DSA_IV_2_REG | IV block data | 0x0638 | WO |
| DSA_IV_3_REG | IV block data | 0x063C | WO |
| DSA_KEY_SOURCE_REG | Configures RSA_DS_KEY source | 0x0E18 | R/W |
| **Status/Control Registers** | | | |
| DSA_SET_START_REG | Activates the RSA_DS peripheral | 0x0E00 | WO |
| DSA_SET_ME_REG | Starts RSA_DS operation | 0x0E04 | WO |
| DSA_SET_FINISH_REG | Ends RSA_DS operation | 0x0E08 | WO |
| DSA_QUERY_BUSY_REG | Status of the RSA_DS peripheral | 0x0E0C | RO |
| DSA_QUERY_KEY_WRONG_REG | Checks the reason why RSA_DS_KEY is not ready | 0x0E10 | RO |
| DSA_QUERY_CHECK_REG | Queries DSA check result | 0x0E14 | RO |
| **Version control register** | | | |
| DSA_DATE_REG | Version control register | 0x0E20 | W/R |