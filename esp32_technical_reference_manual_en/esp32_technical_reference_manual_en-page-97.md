**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Body Text:**

1. Write `0x5A5A` into register EFUSE_CONF.
2. Write `0x2` into register EFUSE_CMD.
3. Poll the register EFUSE_CMD until it is `0x0`, or wait for a program-done interrupt.
4. Write `0xAA55` into register EFUSE_CONF.
5. Write `0x1` into register EFUSE_CMD.
6. Poll register EFUSE_CMD until it is `0x0`, or wait for a read-done interrupt.

**Additional Instructions:**
Set the corresponding register bit of the programmed bit to 0.

The configuration values of the registers are based on current APB_CLK frequency, as shown in Table 5.3-4 below:

**Table Title:** 
Table 5.3-4. Timing Configuration

| Register                | Configuration Value | APB_CLK Frequency |
|-------------------------|--------------------|-------------------|
| EFUSE_CLK              | EFUSE_CLK_SELO[7:0] | 26 MHz            | 40 MHz           | 80 MHz          |
|                       | EFUSE_CLK_SEL1[7:0]| 250               | 160             | 80             |
| EFUSE_DAC_CONF         | EFUSE_DAC_CLK_DIV[7:0] | 255              | 128            |                |

**Instructions for Identifying Program/Read-Done Interrupts (Method One):**
1. Poll bit `1/0` in register EFUSE_INT_RAW until it is `1`, which represents the generation of an program/read-done interrupt.
2. Set the bit `1/0` in register EFUSE_INT_CLR to 1 to clear the program/read-done interrupts.

**Instructions for Identifying Program/Read-Done Interrupts (Method Two):**
1. Set bit `1/0` in register EFUSE_INT_ENA to enable eFuse Controller post a program/read-done interrupt.
2. Configure Interrupt Matrix to enable the CPU to respond to an EFUSE_INT interrupt.
3. A program/read-done interrupt is generated.

**Additional Instructions:**
4. Read bit `1/0` in register EFUSE_INT_ST to identify the generation of the program/read-done interrupt.
5. Set bit `1/0` in register EFUSE_INT_CLR to 1 to clear the program/read-done interrupt.

The programming of different system parameters and even the programming of different bits of the same system parameter can be completed separately in multiple programmings, but it is recommended that users minimize programming cycles by programming all necessary bits at once. After completing one programming action for a certain bit controlled via efuse_wr_disable, this should immediately follow with another program to control other parameters.

Repeated programming of programmed bits is strictly forbidden.
  
**Footer:**
Espressif Systems
Page 97 ESP32 TRM (Version 5.6)
Submit Documentation Feedback