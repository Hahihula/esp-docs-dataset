**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Register Information:**
- Register Name: IO_MUX_X_REG (X: 0-19, 20¹, 21-23, 25-27, 32-39) (See Table 6.12-2 for the addresses)
- Address Bits:
  - 0x0
  - 0x2

**Field Descriptions:**
- MCU_SEL: Selects IO_MUX function for this signal.
  - 0 selects Function 0, 
  - 1 selects Function 1,
  - etc. (R/W)

- FUN_DRV: Select the drive strength of the pin.
  - A higher value corresponds with a higher strength
  - For GPIO34-39, FUN_DRV is always O.

**Notes on ESP32 Pin Lists**: See note in Table 6.12

- MCUbase: In ESP32 Datasheet (R/W)

- FUN_IE: Input enable of the pin.
  - 1: input enabled; 
  - 0: input disabled;
  - etc.

- FUN_WPU: Pull-up enable of the pin
  - Internal pull-up enabled:
    - O: internal pull-up disabled. GPIO pins 34-39 are input-only, these pins do not feature an output driver or internal pull-up/pull-down circuitry.
  - Therefore their FUN_WPU is always O.

- MCUbase: In ESP32 Datasheet (R/W)

- MCUbase: In ESP32 Datasheet

**Field Descriptions for Other Registers:**
- MCUbase
- MCUbase in Chapter 3 System and Memory. The absolute register addresses are listed in Section 6.12.3 RTC IO MUX Register Summary.

**Note at the bottom of page:** 
- GPIO20 is available only on ESP32-PICO-V3 and ESP32-PICO-V3-02

**Section Title:**
6.13.3 RTC IO MUX Registers

**Description for Section 6.13.3:**
The addresses in parenthesis besides register names are the register addresses relative to (the RTC base address + 0x0400 = 0x3FF4_8400). The RTC base address is provided in Table 3.3-6 Peripheral Address Mapping.

**Footer Information:** 
- Espressif Systems
- Page Number: 149
- Document Version: ESP32 TRM (Version 5.6)
- Submit Documentation Feedback