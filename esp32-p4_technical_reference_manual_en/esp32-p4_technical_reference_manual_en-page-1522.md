

```markdown
## 31.4.2.4 Parsing the Message

The message and its padding must be parsed into N 512-bit message blocks: M⁽¹⁾, M⁽²⁾, ..., M⁽ᴺ⁾.

**Note:**
1. For more details about “parsing the message”, please refer to [FIPS PUB 180-4 Spec > Section "Parsing the Message"](https://example.com).
2. For more information on “message block”, please refer to [FIPS PUB 180-4 Spec > Section "Glossary of Terms and Acronyms"](https://example.com).

## 31.4.3 Security Features

To ensure the security of the operation process, the ECDSA_DS module implements a variety of security functions.

### 31.4.3.1 High Anti-Attack Performance

ESP32-P4’s ECDSA_DS module leverages ECC’s enhanced anti-attack performance (refer to Section 26.4.3 Enhancing Anti-Attack Performance) every time it performs an operation. This means that each time a signature is generated and verified by the ECDSA_DS:

* The execution latency is constant for a given operation.
* Power consumption variations are minimized.

This provides ESP32-P4’s ECDSA_DS module strong anti-attack performance.

### 31.4.3.2 State-Dependent Register Access Control

ESP32-P4’s ECDSA_DS module has implemented a state-dependent register access control mechanism to prevent any possibility of key theft by tampering with the configuration or accessing the data during the operation.

By implementing the state-dependent register access control, the accesses for ECDSA_DS registers are designed to vary in different states. For example, `ECDSA_CONF_REG` is only available for reading and writing when ECDSA_DS is in the IDLE state. In this way, the configuration information is protected from reading or writing when ECDSA_DS is in other states, such as LOAD and BUSY. For details about all ECDSA_DS working states, please refer to Table 31.4-3.

For detailed information on the state-dependent access control of each ECDSA_DS register, please refer to Section Register Summary.

### 31.4.3.3 Hardware Occupation

During the operation, the following hardware modules will be occupied by ESP32-P4’s ECDSA_DS module:

* SHA Accelerator
* ECC Accelerator
```