

```markdown
Chapter 28

RSA Accelerator (RSA)

28.1 Introduction

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly improving their run time and reducing their software complexity compared with RSA algorithms implemented solely in software. The RSA accelerator also supports operands of different lengths, which provides more flexibility during the computation.

28.2 Features

The following functionality is supported:

* Large-number modular exponentiation with two additional acceleration options to further increase the calculation speed
* Large-number modular multiplication
* Large-number multiplication
* Operands of different lengths
* Interrupt on completion of computation

28.3 Functional Description

The RSA accelerator is activated by setting the HP_SYS_CLKRST_REG_CRYPTO_RSA_CLK_EN bit in the HP_SYS_CLKRST_PERI_CLK_CTRL25_REG register and clearing the HP_SYS_CLKRST_REG_RST_EN_RSA bit in the HP_SYS_CLKRST_HP_RST_EN2_REG register. Additionally, users also need to clear HP_SYS_CLKRST_REG_RST_EN_DS and HP_SYS_CLKRST_REG_RST_EN_ECDSA bits to reset the RSA Digital Signature Peripheral (RSA_DS) and the ECDSA Digital Signature Peripheral (ECDSA_DS) accelerators.

The RSA accelerator is only available after the RSA-related memories are initialized. The content of the RSA_QUERY_CLEAN_REG register is 0 during initialization and will become 1 after the initialization is done. Therefore, wait until RSA_QUERY_CLEAN_REG becomes 1 before using the RSA accelerator.

The RSA_INT_ENA_REG register is used to control the interrupt triggered on completion of computation. Write 1 or 0 to this field to enable or disable the interrupt. By default, the interrupt function of the RSA accelerator is enabled.

Notice:
ESP32-P4's RSA Digital Signature Peripheral (RSA_DS) and ECDSA Digital Signature Peripheral (ECDSA_DS) modules
```