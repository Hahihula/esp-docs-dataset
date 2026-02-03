**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header:**
Register 6.18. GPIO_PINn_REG (n): O-48 (0x0074+0x4*n)

**Binary Representation Table:**
| Bit | Value |
|-----|-------|
| 31  | 0     |
| ... | ...   |

**Description of Register:**
GPIO_PINn_SYNC2_BYPASS  
For the second stage synchronization, GPIO input data can be synchronized on either edge of the APB clock. O: no synchronization; 1: synchronized on falling edge; and 3: synchronized on rising edge.

**Register Description:**
GPIO_PINn_PAD_DRIVER  
Pin driver selection. O: normal output; 1: open drain output.
R/W

**Description for Register:**
For the first stage synchronization, GPIO input data can be synchronized on either edge of the APB clock. O: no synchronization; 1: synchronized on falling edge and rising edge.

**Other Registers Descriptions (partially visible):**

- **GPIO_PINn_SYNC1_BYPASS:** 
  For the second stage synchronization.
  
- **GPIO_PINn_INT_TYPE:** 
  Interrupt type selection
  
- **GPIO_PINn_WAKEUP_ENABLE:** 
  GPIO wake-up enable bit, only wakes up the CPU from Light-sleep.

**Additional Registers:**

- **GPIO_PINn_CONFIG**
  Reserved (R/W)

- **GPIO_PINn_INT_ENA**
  Interrupt enable bits. bit13: CPU interrupt enabled; bit14: CPU non-maskable interrupt enabled.
  
- **GPIO_FUNCy_IN_SEL_CFG_REG:** 
  Selection control for peripheral input signal, selects a pin from the 48 GPIO matrix pins to connect this input signal.

**Additional Information about Registers (partially visible):**

- **GPIO_SIGy_IN_SEL**
  Bypasses GPIO matrix. 

- **GPIOFuncy_IN_INV_SEL:**
  Invert the input value; O: Do not invert the input value.
  
- **GPIO_SIGy_INInv_SEL:**
  Invert or route signals via GPIO matrix.

**Footer Information:** 
Espressif Systems
507 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback