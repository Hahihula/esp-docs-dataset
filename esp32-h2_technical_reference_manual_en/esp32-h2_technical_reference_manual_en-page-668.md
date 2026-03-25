

```markdown
Chapter 25 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


For more details about "parsing the message", please refer to FIPS PUB 180-4 Spec > Section "Parsing the Message".

For more information about "message block", please refer to FIPS PUB 180-4 Spec > Section "Glossary of Terms and Acronyms".


## 25.4.3 Security Features

To ensure the security of the ECDSA operation process, the ECDSA accelerator implements a variety of security functions.

### 25.4.3.1 High Anti-Attack Performance

ESP32-H2's ECDSA accelerator leverages ECC's enhanced anti-attack performance (refer to Section 20.4.3 Enhancing Anti-Attack Performance) every time it performs an operation. This means that each time a signature is generated and verified, ECDSA consumes:

* the same amount of time;
* the same amount of power.

This provides ESP32-H2's ECDSA accelerator strong anti-attack performance.

### 25.4.3.2 Dynamic Access Permission

ESP32-H2's ECDSA accelerator has implemented a dynamic access permission mechanism to prevent any possibility of key theft by tampering with the configuration or accessing the data during the operation.

By implementing this dynamic access permission mechanism, the accesses for ECDSA registers are designed to vary in different statuses. For example, ECDSA_CONF_REG is only available for reading and writing when the accelerator is in the IDLE status. In this way, the configuration information is protected from reading or writing when the accelerator is in other statuses, such as LOAD, GAIN and BUSY. For details about all ECDSA working statues, please refer to Table 25.4-4.

For detailed information about the dynamic access permission of each ECDSA register, please refer to Section Register Summary.

### 25.4.3.3 Hardware Occupation

During the ECDSA operation, the following hardware modules will be occupied by ESP32-H2's ECDSA accelerator:

* SHA Accelerator
* RSA Accelerator
* ECC Accelerator

Among them, the SHA accelerator will be released when the ECDSA_SHA_RELEASE_INT is triggered. While, the RSA accelerator and the ECC accelerator will be occupied during the whole ECDSA operation.

**Note:**
Hardware occupation is a mechanism to protect multiplexed modules and storage space. When a module is hardware
```