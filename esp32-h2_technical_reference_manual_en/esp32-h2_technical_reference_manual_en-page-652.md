

```markdown
Chapter 24 Digital Signature Algorithm (DSA)

GoBack

Chapter 24

Digital Signature Algorithm (DSA)

24.1 Overview

The Digital Signature Algorithm (DSA) is used to verify the authenticity and integrity of a message using a cryptographic algorithm. This can be used to validate a device's identity to a server or to check the integrity of a message.

ESP32-H2 includes a Digital Signature Algorithm (DSA) module providing hardware acceleration of messages' signatures based on RSA. HMAC is used as the key derivation function (KDF) to output the DSA_KEY key using a key stored in eFuse as the input key. Subsequently, the DSA module uses DSA_KEY to decrypt the pre-encrypted parameters and calculate the signature. The whole process happens in hardware so that neither the decryption key for the RSA parameters nor the input key for the HMAC key derivation function can be seen by users while calculating the signature.

24.2 Features

*   RSA digital signatures with key length up to 3072 bits
*   Encrypted private key data, only decryptable by the DSA module
*   SHA-256 digest to protect private key data against tampering by an attacker

24.3 Functional Description

24.3.1 Overview

The DSA peripheral calculates RSA signatures as Z = X^Y mod M, where Z is the signature, X is the input message, and Y and M are the RSA private key parameters.

Private key parameters are stored in flash as ciphertext. They are decrypted using a key (DSA_KEY) which can only be calculated by the DSA peripheral via the HMAC peripheral. The required inputs (HMAC_KEY) to generate the key are only stored in eFuse and can only be accessed by the HMAC peripheral. That is to say, the DSA peripheral hardware can decrypt the private key, and the private key in plaintext is never accessed by the software. For more detailed information about eFuse and HMAC peripherals, please refer to Chapter 5 eFuse Controller (EFUSE) and Chapter 21 HMAC Accelerator (HMAC).

The input message X will be sent directly to the DSA peripheral by the software each time a signature is needed. After the RSA signature operation, the signature Z is read back by the software.

For better understanding, we define some symbols and functions here, which are only applicable to this chapter:
```