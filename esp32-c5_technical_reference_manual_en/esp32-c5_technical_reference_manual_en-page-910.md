

```markdown
Chapter 25  
RSA Accelerator (RSA)

25.1 Introduction

The RSA accelerator provides hardware support for high-precision computation used in various RSA asymmetric cipher algorithms, significantly reducing their run time and reducing their software complexity. Compared with RSA algorithms implemented solely in software, this hardware accelerator can speed up RSA algorithms significantly. The RSA accelerator also supports operands of different lengths, which provides more flexibility during the computation.

25.2 Features

The following functionality is supported:

* Large-number modular exponentiation with two acceleration options
* Large-number modular multiplication
* Large-number multiplication
* Operands of different lengths
* Interrupt on completion of computation

25.3 Functional Description

The RSA accelerator is activated by setting the `PCR_RSA_CLK_EN` bit and clearing the `PCR_RSA_RST_EN` bit in the `PCR_RSA_CONF_REG` register. Additionally, users also need to clear `PCR_DS_RST_EN` and `PCR_ECDSA_RST_EN` bits to reset Digital Signature Algorithm (DSA) and Elliptic Curve Digital Signature Algorithm (ECDSA).

The RSA accelerator is only available after the RSA-related memories are initialized. The content of the `RSA_QUERY_CLEAN_REG` register is 0 during initialization and will become 1 after the initialization is done. Therefore, wait until `RSA_QUERY_CLEAN_REG` becomes 1 before using the RSA accelerator.

The `RSA_INT_ENA_REG` register is used to control the interrupt triggered on completion of computation. Write 1 or 0 to this field to enable or disable the interrupt. By default, the interrupt function of the RSA accelerator is enabled.

Notice:
ESP32-C5's Digital Signature Algorithm (DSA) module also calls the RSA accelerator when working. Therefore, users cannot access the RSA accelerator when the Digital Signature Algorithm (DSA) module is working.
```