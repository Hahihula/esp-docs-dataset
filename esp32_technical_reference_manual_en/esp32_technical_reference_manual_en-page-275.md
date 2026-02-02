**Chapter Title:**
Chapter 13 Process ID Controller (PID)

**Body Text:**
specified in register PIDCTRL_PID_DELAY_REG and PIDCTRL_NMI_DELAY_REG respectively.

In step 7, other tasks can be implemented as well. To do this, the cost of those tasks should be included when configuring registers PIDCTRL_PID_DELAY_REG and PIDCTRL_NMI_DELAY_REG in step 3.

**Subtitle:**
13.4 Register Summary

**Table:**

| Name                          | Description                                                                                   | Address            | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|--------------------|--------|
| PIDCTRL_INTERRUPT_ENABLE_REG | PID interrupt identification enable                                                          | 0x3FF1F000         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_1_REG | Level 1 interrupt vector address                                                             | 0x3FF1F004         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_2_REG | Level 2 interrupt vector address                                                             | 0x3FF1F008         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_3_REG | Level 3 interrupt vector address                                                             | 0x3FF1F00C         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_4_REG | Level 4 interrupt vector address                                                             | 0x3FF1F010         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_5_REG | Level 5 interrupt vector address                                                             | 0x3FF1F014         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_6_REG | Level 6 interrupt vector address                                                             | 0x3FF1F018         | R/W    |
| PIDCTRL_INTERRUPT_ADDR_7_REG | NMI interrupt vector address                                                                | 0x3FF1F01C         | R/W    |
| PIDCTRL_PID_DELAY_REG        | New PID valid delay                                                                          | 0x3FF1F020         | R/W    |
| PIDCTRL_NMI_DELAY_REG        | NMI mask signal disable                                                                       | 0x3FF1F024         | R/W    |
| PIDCTRL_LEVEL_REG            | Current interrupt priority                                                                   | 0x3FF1F028         | R/W    |
| PIDCTRL_FROM_1_REG          | System status before Level 1 interrupt                                                      | 0x3FF1F02C         | R/W    |
| PIDCTRL_FROM_2_REG          | System status before Level 2 interrupt                                                      | 0x3FF1F030         | R/W    |
| PIDCTRL_FROM_3_REG          | System status before Level 3 interrupt                                                      | 0x3FF1F034         | R/W    |
| PIDCTRL_FROM_4_REG          | System status before Level 4 interrupt                                                      | 0x3FF1F038         | R/W    |
| PIDCTRL_FROM_5_REG          | System status before Level 5 interrupt                                                      | 0x3FF1F03C         | R/W    |
| PIDCTRL_FROM_6_REG          | System status before Level 6 interrupt                                                      | 0x3FF1F040         | R/W    |
| PIDCTRL_FROM_7_REG          | System status before NMI                                                                       | 0x3FF1F044         | R/W    |
| PIDCTRL_PID_NEW_REG         | New PID configuration register                                                               | 0x3FF1F048         | R/W    |
| PIDCTRL_PID_CONFIRM_REG     | New PID confirmation register                                                                | 0x3FF1F04C         | WO     |
| PIDCTRL_NMI_MASK_ENABLE_REG | NMI mask enable register                                                                     | 0x3FF1F054         | WO     |
| PIDCTRL_NMI_MASK_DISABLE_REG| NMI mask disable register                                                                    | 0x3FF1F058         | WO     |

**Subtitle:**
13.5 Registers

**Body Text:**
The addresses in parenthesis besides register names are the register addresses relative to the PID Controller base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section **13.4 Register Summary**.

**Footer:**
Espressif Systems

**Page Number:** 
275

**Document Version:**
ESP32 TRM (Version 5.6)

**Link Texts:**
- Submit Documentation Feedback
- GoBack