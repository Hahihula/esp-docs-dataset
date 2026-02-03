**Title:**
Chapter 16 World Controller (WCL)

**Subtitle:**
16.6 NMI Interrupt Masking

**Body Text:**

Some software process of ESP32-S3 should not be interrupted. For example, the configuration of World Controller should not be interrupted by any interrupts, including the NMI interrupts.

Normally, we can configure some CPU registers to mask different kinds of interrupts, but NMI interrupt is not one of them. To mask an NMI interrupt, you need to configure the interrupt sources, which is more complicated. For details, see Chapter 9 Interrupt Matrix (INTERRUPT).

World Controller has implemented some hardware mechanism to simplify the process to mask NMI interrupts for:

- **All applications:**
  - Configure WCL_CORE_m_NMI_MASK:
    * Enable
    * Disable

- **Some applications:**
  1. Configures WCL CORE m NMI MASK TRIGGER ADDR to the address at which the NMI interrupt masking ends, meaning the CPU stops masking NMI interrupts after this address.
  2. Write any value to WCL CORE m NMI MASK DISABLE, indicating the completion of TRIGGER_ADDR configuration.
  3. Write any value to WCL CORE m NMI MASK ENABLE to start masking NMI interrupts till the address configured in WCL CORE m NMI MASK TRIGGER ADDR.

**Note:**
- Only one of the above two methods should be used at the same time.
- The configuration to mask NMI interrupts is effective all the time until trigger address executes. Therefore, you need to configure the world controller to mask NMI interrupts again once trigger address executes.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
811 ESP32-S3 TRM (Version 1.7)