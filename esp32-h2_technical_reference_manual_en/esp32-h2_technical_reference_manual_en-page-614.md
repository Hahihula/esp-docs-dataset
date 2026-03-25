

```markdown
Chapter 21 HMAC Accelerator (HMAC)
```

## Chapter 21

### HMAC Accelerator (HMAC)

The Hash-based Message Authentication Code (HMAC) module computes Message Authentication Codes (MACs) using Hash algorithm SHA-256 and keys as described in RFC 2104. The 256-bit HMAC key is stored in an eFuse key block and can be set as read-protected, i.e., the key is not accessible from outside the HMAC accelerator.

#### 21.1 Main Features

* Standard HMAC-SHA-256 algorithm
* Hash result only accessible by configurable hardware peripheral (in downstream mode)
* Compatibility with challenge-response authentication algorithm
* Generates required keys for the Digital Signature Algorithm (DSA) peripheral (in downstream mode)
* Re-enables soft-disabled JTAG (in downstream mode)

#### 21.2 Functional Description

The HMAC module operates in two modes: upstream mode and downstream mode. In upstream mode, users provide the HMAC message and read back the calculation result. In downstream mode, the HMAC module is used as a Key Derivation Function (KDF) for other internal hardware. For instance, the JTAG can be temporarily disabled by burning odd number bits of `EFUSE_SOFT_DIS_JTAG` in eFuse. In this case, users can temporarily re-enable JTAG using the HMAC module in downstream mode.

After the reset signal being released, the HMAC module will check whether the DSA key exists in the eFuse. If the key exists, the HMAC module will enter downstream digital signature algorithm mode and finish the DSA key calculation automatically.

##### 21.2.1 Upstream Mode

Common use cases for the upstream mode are challenge-response protocols supporting HMAC-SHA-256. Assume the two entities in the challenge-response protocol are A and B respectively, and the data message they expect to exchange is M. The general authentication process of this protocol is as follows:

* A calculates a unique random number M.
* A sends M to B.
* B calculates the HMAC (through M and KEY) and sends the result to A.
* A calculates the HMAC (through M and KEY) internally.
```