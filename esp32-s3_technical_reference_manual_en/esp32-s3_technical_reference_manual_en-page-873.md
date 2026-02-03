**Chapter Title:**
Chapter 20 RSA Accelerator (RSA)

**GoBack Link:** [GoBack](#)

---

### Section Heading:
RSA Accelerator (RSA)

#### Subsection 20.1 Introduction

The RSA Accelerator provides hardware support for high precision computation used in various RSA asymmetric cipher algorithms by significantly reducing their software complexity. Compared with RSA algorithms implemented solely in software, this hardware accelerator can speed up RSA algorithms significantly. Besides, the RSA Accelerator also supports operands of different lengths, which provides more flexibility during the computation.

#### Subsection 20.2 Features

The following functionality is supported:
- Large-number modular exponentiation with two optional acceleration options
- Large-number modular multiplication
- Large-number multiplication
- Operands of different lengths
- Interrupt on completion of computation

#### Subsection 20.3 Functional Description

The RSA Accelerator is activated by setting the `SYSTEM_CRYPTO_RSA_CLK_EN` bit in the `SYSTEM_PERIP_CLK_EN1_REG` register and clearing the `SYSTEM_RSA_MEM_PD` bit in the `SYSTEM_RSA_PD_CTRL_REG` register. This releases the RSA Accelerator from reset.

The RSA Accelerator is only available after the `RSA-related memories` are initialized. The content of the `RSA_CLEAN_REG` register is 0 during initialization and will become 1 after the initialization is done. Therefore, it is advised to wait until `RSA_CLEAN_REG` becomes 1 before using the RSA Accelerator.

The `RSA_INTERRUPT_ENA_REG` register is used to control the interrupt triggered on completion of computation. Write 1 or 0 to this register to enable or disable interrupt. By default, the interrupt function of the RSA Accelerator is enabled.

#### Notice:
ESP32-S3's Digital Signature (DS) module also calls the rsa accelerator. Therefore, users cannot access the RSA accelerator when Digital Signature (DS) is working.

---

**Footer:**
Espressif Systems  
Page 873 ESP32-S3 TRM (Version 1.7)

[Submit Documentation Feedback](#)