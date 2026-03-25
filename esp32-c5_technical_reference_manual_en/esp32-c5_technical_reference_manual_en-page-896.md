

```markdown
Chapter 24 HMAC Accelerator (HMAC)

## Chapter 24

### HMAC Accelerator (HMAC)

#### 24.1 Overview

The Hash-based Message Authentication Code (HMAC) module computes Message Authentication Codes (MACs) using hash algorithm SHA-256 and keys as described in RFC 2104. The 256-bit HMAC key is stored in an eFuse key block and can be set as read-protected, i.e., the key is not accessible from outside the HMAC accelerator.

#### 24.2 Feature List

* Standard HMAC-SHA-256 algorithm
* HMAC-SHA-256 calculation based on key in eFuse,
    - whose result cannot be accessed by software in downstream mode for high security
    - whose result can be accessed by software in upstream mode
* Generates required keys for the Digital Signature Algorithm (DSA) peripheral in downstream mode
* Re-enables soft-disabled JTAG in downstream mode

#### 24.3 Functional Description

The HMAC module operates in two modes: upstream mode and downstream mode. In upstream mode, users provide the HMAC message and read back the calculation result. In downstream mode, the HMAC module provides input to two possible other internal hardware modules: On the one hand, an HMAC can be used to enable JTAG after JTAG has been temporarily disabled before. On the other hand, an HMAC can be used as the decryption key for Digital Signature parameters stored in the memory for the DSA peripheral. Furthermore, the calculations happen internally and automatically in downstream mode, so that confidentiality of any key and derived key material is ensured, given correct configuration.

**Note:**
After the reset signal being released, the HMAC module will check whether the DSA key exists in the eFuse. If the key exists, the HMAC module will enter downstream digital signature algorithm mode and finish the DSA key calculation automatically. This process is automatically completed by hardware and does not require software participation. When the downstream operation after reset is completed, the HMAC will automatically return to the idle state.
```