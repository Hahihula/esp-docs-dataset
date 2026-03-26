

# Chapter 27

## HMAC Accelerator (HMAC)

The Hash-based Message Authentication Code (HMAC) module computes Message Authentication Codes (MACs) using hash algorithm SHA-256 and keys as described in RFC 2104. The 256-bit HMAC key is stored in an eFuse key block and can be set as read-protected, i.e., the key is not accessible from outside the HMAC accelerator.

### 27.1 Main Features

* Standard HMAC-SHA-256 algorithm
* HMAC-SHA-256 calculation based on key in eFuse,
    - whose result cannot be accessed by software in downstream mode for high security
    - whose result can be accessed by software in upstream mode
* Generates required keys for the RSA Digital Signature Peripheral (RSA_DS) in downstream mode
* Re-enables soft-disabled JTAG in downstream mode

### 27.2 Functional Description

The HMAC module operates in two modes: upstream mode and downstream mode. In upstream mode, users provide the HMAC message and read back the calculation result. In downstream mode, the HMAC module provides input to two possible other internal hardware modules: On the one hand, an HMAC can be used to enable JTAG after JTAG has been temporarily disabled before. On the other hand, an HMAC can be used as decryption key for Digital Signature parameters stored in flash memory for the RSA_DS peripheral. Furthermore, the calculations happen internally and automatically in downstream mode, so that confidentiality of any key and derived key material is ensured, given correct configuration.

**Note:**
After the reset signal being released, the HMAC module will check whether the RSA_DS_KEY exists in the eFuse. If the key exists, the HMAC module will enter downstream RSA_DS mode and finish the RSA_DS_KEY calculation automatically. This process is automatically completed by hardware and does not require software participation. When the downstream operation after reset is completed, the HMAC will automatically return to the idle state.

#### 27.2.1 Upstream Mode

To calculate the HMAC value in upstream mode, users should perform the following steps:

1. Initialize the HMAC module and enter upstream mode.