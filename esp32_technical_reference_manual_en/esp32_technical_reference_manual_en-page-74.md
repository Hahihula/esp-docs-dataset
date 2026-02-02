**Chapter Title:**
Chapter 3 System and Memory

**GoBack Link:** GoBack

---

### Subsection Titles:

#### **3.3.5.1 Asymmetric PID Controller Peripheral**

- There are two PID Controllers in the system.
- They serve the PRO_CPU and the APP_CPU, respectively.

The PRO_CPU and the APP_CPU can only access their own PID Controller and not that of their counterpart.
Each CPU uses the same memory range 0x3FF1_F000 ~ 3FF1_FFFF to access its own PID Controller.

#### **3.3.5.2 Non-Contiguous Peripheral Memory Ranges**

The SDIO Slave peripheral consists of three parts and the two CPUs use non-contiguous addresses to access these.
The three parts are accessed at the address ranges:
0x3FF4_B000 ~ 3FF4_BFFF, 
0x3FF5_5000 ~ 3FF5_5FFF,
and Ox3FF5_8000 ~ 3FF5_8FFF of each CPU's data bus.
Similarly to other peripherals, access to this peripheral is identical for both CPUs.

#### **3.3.5.3 Memory Speed**

The ROM as well as the SRAM are both clocked from CPU_CLK and can be accessed by the CPU in a single cycle.
The RTC FAST memory is clocked from APB_CLOCK and the RTC SLOW memory from the FAST_CLOCK, so access to these memories may be slower.

DMA uses the APB_CLK to access memory. Internally, the SRAM is organized into 32K-sized banks.
Each CPU and DMA channel can simultaneously access the SRAM at full speed,
provided they access addresses in different memory banks.

---

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)