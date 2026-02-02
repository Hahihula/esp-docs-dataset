**Chapter Title:**
Chapter 8 Interrupt Matrix (INTERRUPT)

**Body Text:**

- **PRO_X_MAP_REG** or APP_X_MAP_REG stands for any particular peripheral interrupt configuration register of the PRO_CPU (or APP_CPU). The peripheral interrupt configuration register corresponds to the peripheral interrupt source Source_X. In Table 8.3-1, the registers listed under "PRO_CPU (APP_CPU) - Peripheral Interrupt Configuration Register" correspond to the peripheral interrupt sources listed in “Peripheral Interrupt Source - Name”.

**Interrupt_P** stands for CPU peripheral interrupt, numbered as Num_P. Num_P can take the ranges 0 ~ 5, 8 ~ 10, 12 ~ 14, 17 ~ 28, 30 ~ 31.

**Interrupt_I** stands for the CPU internal interrupt numbered as Num_I. Num_I can take values 6, 7, 11, 15, 16, 29.

Using this terminology, the possible operations of the Interrupt Matrix controller can be described as follows:

- **Allocate peripheral interrupt source Source_X to CPU (PRO_CPU or APP_CPU)**
  Set PRO_X_MAP_REG (or APP_X_MAP_REG) to Num_P. Num_P can be any CPU peripheral interrupt number. CPU interrupts can be shared between multiple peripherals (see below).

- **Disable peripheral interrupt source X for CPU (PRO_CPU or APP_CPU)**
  Set PRO_X_MAP_REG (or APP_X_MAP_REG) for peripheral interrupt source to any Num_I. The specific choice of internal interrupt number does not change behavior, as none of the interrupt numbered as Num_I is connected to either CPU.

- **Allocate multiple peripheral sources Source_Xn ORed to PRO_CPU (APP_CPU) peripheral interrupt**
  Set multiple PRO_Xn_MAP_REG (APP_Xn_MAP_REG) to the same Num_P. Any of these peripheral interrupts will trigger CPU Interrupt_P.

**Subsections:**

8.3.4 **CPU NMI Interrupt Mask**
The Interrupt Matrix temporarily masks all peripheral interrupt sources allocated to PRO_CPU’s or APP_CPU's NMI interrupt, if it receives the signal PRO_CPU NMI Interrupt Mask (or APP_CPU NMI Interrupt Mask) from the peripheral PID Controller, respectively.

8.3.5 **Query Current Interrupt Status of Peripheral Interrupt Source**
The current interrupt status of a peripheral interrupt source can be read via the bit value in PRO_INR_STATUS_REG_n (APP_INR_STATUS_REG_n), as shown in the mapping in Table 8.3-1.

**Section Title:**

8.4 Registers

The interrupt matrix registers are part of the DPORT registers and are described in Section 12.4 in Chapter 12 [DPort Registers](#).

**Footer Information:**
Espressif Systems
Page number: 179
Document version: ESP32 TRM (Version 5.6)
Link to Submit Documentation Feedback