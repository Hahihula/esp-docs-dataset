

```markdown
Chapter 27 Digital Signature Algorithm (DSA)

GoBack

Chapter 27

Digital Signature Algorithm (DSA)

27.1 Overview

The Digital Signature Algorithm (DSA) is used to verify the authenticity and integrity of a message using a cryptographic algorithm. This can be used to validate a device's identity to a server or to check the integrity of a message.

ESP32-C5 includes a Digital Signature Algorithm (DSA) module providing hardware acceleration of messages' signatures based on RSA. HMAC is used as the key derivation function (KDF) to output the DSA_KEY key using a key stored in eFuse or deployed by the Key Manager as the input key. Subsequently, the DSA module uses DSA_KEY to decrypt the pre-encrypted parameters and calculate the signature. The whole process happens in hardware so that neither the decryption key for the RSA parameters nor the input key for the HMAC key derivation function can be seen by users while calculating the signature.

27.2 Features

*   RSA digital signatures with key length up to 3072 bits
*   Encrypted private key data, only decryptable by the DSA module
*   SHA-256 digest to protect private key data against tampering by an attacker

27.3 Functional Description

27.3.1 Overview

The DSA peripheral calculates RSA signatures as Z = X^Y mod M, where Z is the signature, X is the input message, and Y and M are the RSA private key parameters.

Private key parameters are stored in flash as ciphertext. They are decrypted using a key (DSA_KEY) which can:

*   Only be calculated by the DSA peripheral via the HMAC peripheral. The required inputs (HMAC_KEY) to generate the key (DSA_KEY) are only stored in eFuse and can only be accessed by the HMAC peripheral. That is to say, the DSA peripheral hardware can decrypt the private key, and the private key in plaintext is never accessed by the software. For more detailed information about eFuse and HMAC peripherals, please refer to Chapter 7 eFuse Controller (EFUSE) and Chapter 24 HMAC Accelerator (HMAC).
*   Deploy from Key Manager module. The DSA_KEY must be deployed by the Key Manager in a secured way.
```