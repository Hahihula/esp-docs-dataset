

```markdown
Note:
1. For more details about "parsing the message", please refer to FIPS PUB 180-4 Spec > Section "Parsing the Message".
2. For more information on "message block", please refer to FIPS PUB 180-4 Spec > Section "Glossary of Terms and Acronyms".

## 22.4.3 Security Features

To ensure the security of the ECDSA operation process, the ECDSA accelerator implements a variety of security functions.

### 22.4.3.1 High Anti-Attack Performance

ESP32-C61's ECDSA accelerator leverages ECC's enhanced anti-attack performance (refer to Section 20.4.3 Enhancing Anti-Attack Performance) every time it performs an operation. This means that each time a signature is generated and verified by the ECDSA accelerator:

* The execution latency is constant for a given operation.
* Power consumption variations are minimized.

This provides ESP32-C61's ECDSA accelerator strong anti-attack performance.

### 22.4.3.2 State-Dependent Register Access Control

ESP32-C61's ECDSA accelerator has implemented a state-dependent register access control mechanism to prevent any possibility of key theft by tampering with the configuration or accessing the data during the operation.

By implementing the state-dependent register access control, the accesses for ECDSA registers are designed to vary in different states. For example, `ECDSA_CONF_REG` is only available for reading and writing when the accelerator is in the IDLE state. In this way, the configuration information is protected from reading or writing when the accelerator is in other states, such as LOAD, GAIN, and BUSY. For details about all ECDSA working states, please refer to Table 22.4-4.

For detailed information on the state-dependent access control of each ECDSA register, please refer to Section Register Summary.

### 22.4.3.3 Hardware Occupation

During the ECDSA operation, the following hardware modules will be occupied by ESP32-C61's ECDSA accelerator:

* SHA Accelerator
* ECC Accelerator

Among them, the SHA accelerator will be released when `ECDSA_SHA_RELEASE_INT` is triggered, while the ECC accelerator will be occupied during the whole ECDSA operation.
```