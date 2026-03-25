

```markdown
1. First, append the bit "1" to the end of the message;
2. Second, append $L_A$ bits of zeros, where $L_A$ is the smallest, non-negative solution to the equation $L_M + 1 + L_A \equiv 448 \mod 512$;
3. Last, append the 64-bit block of value equal to the number $L_M$ expressed using a binary representation.

For more details, please refer to FIPS PUB 180-4 Spec > Section "Padding the Message".

### 28.4.2.4 Parsing the Message

The message and its padding must be parsed into $N$ 512-bit message blocks: $M^{(1)}, M^{(2)}, ..., M^{(N)}$.

**Note:**
1. For more details about "parsing the message", please refer to FIPS PUB 180-4 Spec > Section "Parsing the Message".
2. For more information on "message block", please refer to FIPS PUB 180-4 Spec > Section "Glossary of Terms and Acronyms".

### 28.4.3 Security Features

To ensure the security of the ECDSA operation process, the ECDSA accelerator implements a variety of security functions.

#### 28.4.3.1 High Anti-Attack Performance

ESP32-C5's ECDSA accelerator leverages ECC's enhanced anti-attack performance (refer to Section 23.4.3 Enhancing Anti-Attack Performance) every time it performs an operation. This means that each time a signature is generated and verified by the ECDSA accelerator:

* The execution latency is constant for a given operation.
* Power consumption variations are minimized.

This provides ESP32-C5's ECDSA accelerator strong anti-attack performance.

#### 28.4.3.2 State-Dependent Register Access Control

ESP32-C5's ECDSA accelerator has implemented a state-dependent register access control mechanism to prevent any possibility of key theft by tampering with the configuration or accessing the data during the operation.

By implementing the state-dependent register access control, the accesses for ECDSA registers are designed to vary in different states. For example, `ECDSA_CONF_REG` is only available for reading and writing when the accelerator is in the IDLE state. In this way, the configuration information is protected from reading or writing when the accelerator is in other states, such as LOAD, GAIN, and BUSY. For details about all ECDSA working states, please refer to Table 28.4-4.

For detailed information on the state-dependent access control of each ECDSA register, please refer to Section Register Summary.
```