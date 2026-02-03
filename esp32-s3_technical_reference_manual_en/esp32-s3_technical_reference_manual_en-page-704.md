**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Section Titles and Content:**

1. **Lock Registers**
   - PMS_CORE_m_VCEBASE_OVERRIDE_2_REG

2. **Lock Internal SRAM’s Usage and Access Configuration**
   - PMS_INTERNAL_SRAM USAGE O REG
     - Related Permission Control Registers:
       - PMS_INTERNAL_SRAM USAGE 0 REG
       - PMS_INTERNAL_SRAM USAGE 1 REG
       - PMS_INTERNAL_SRAM USAGE 2 REG

3. **PMS_CORE_X_IRAMO_PMS CONSTRAIN O REG**
   - Related Permission Control Registers:
     - PMS_CORE_X_IRAMO PMS CONSTRAIN 0 REG
     - PMS CORE m IRAMO PMS CONSTRAIN 1 REG
     - PMS CORE m IRAMO PMS CONSTRAIN 2 REG

4. **PMS CORE m MONITOR O REG**
   - Related Permission Control Registers:
     - PMS CORE m MONITOR 0 REG
     - PMS CORE m DRAMO PMS MONITOR 1 REG

5. **Lock Internal SRAM’s Split Lines Configuration**
   - PMS CORE X IRAMO DRAMO DMA CONSTRAIN O REG
     - Related Permission Control Registers:
       - PMS CORE X IRAMO DRAMO DMA CONSTRAIN O REG
       - PMS CORE X IRAMO DRAMO DMA CONSTRAIN 1 REG

6. **Lock CPU’s Permission to Different Peripheral**
   - PMS CORE m PIF PMS CONSTRAIN O REG (n: 1-5)
     - Related Permission Control Registers:
       - PMS CORE m PIF PMS CONSTRAIN O REG
       - PMS CORE m PIF PMS CONSTRAIN n REG

7. **PMS CORE m REGION PMS CONSTRAIN O REG**
   - Related Permission Control Registers:
     - PMS CORE m REGION PMS CONSTRAIN 0 REG (n: 1-4)
     - PMS CORE m PIF PMS CONSTRAIN O REG
     - PMS CORE m PIF PMS CONSTRAIN n REG

8. **Lock Peripherals’ GDMA Access to Internal SRAM**
   - Related Permission Control Registers:
     - PMS DMA APBPERI SPI2 CONSTRAIN 0 REG (n: 1-6)
       - PMS_DMA_APBPERI_SPI2_PMS CONSTRAIN O REG
       - PMS_DMA_APBPERI_SPI2_PMS CONSTRAIN 1 REG

9. **PMS_DMA_APBPERI SPI3 CONSTRAIN O REG**
   - Related Permission Control Registers:
     - PMS_DMA_APBPERI SPI3 PMS CONSTRAIN O REG (n: 1-6)
       - PMS_DMA_APBPERI SPI3_PMS CONSTRAIN 0 REG
       - PMS_DMA_APBPERI SPI3_PMS CONSTRAIN 1 REG

10. **PMS_DMA_APBPERI I2SO CONSTRAIN O REG**
    - Related Permission Control Registers:
      - PMS_DMA_APBPERI I2SO PMS CONSTRAIN O REG (n: 1-6)
        - PMS_DMA_APBPERI I2SO_PMS CONSTRAIN 0 REG
        - PMS_DMA_APBPERI I2SO1 PMS CONSTRAIN O REG

11. **PMS_DMA_APBPERI AES CONSTRAIN O REG**
    - Related Permission Control Registers:
      - PMS_DMA_APBPERI AES PMS CONSTRAIN O REG (n: 1-6)
        - PMS_DMA_APBPERI AES_PMS CONSTRAIN 0 REG
        - PMS_DMA_APBPERI AES SHA PMS CONSTRAIN O REG

12. **PMS_DMA_APBPERI SHA CONSTRAIN O REG**
    - Related Permission Control Registers:
      - PMS_DMA_APBPERI SHA PMS CONSTRAIN O REG (n: 1-6)
        - PMS_DMA_APBPERI SHA_PMS CONSTRAIN 0 REG
        - PMS_DMA_APBPERI ADC DAC PMS CONSTRAIN O REG

**Footer Information:**
Espressif Systems  
Page number and document version:
704 ESP32-S3 TRM (Version 1.7)  

**Navigation Links:** 
- GoBack