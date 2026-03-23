

```markdown
Chapter 24 Digital Signature (DS)

GoBack

Chapter 24

Digital Signature (DS)

24.1 Overview

A Digital Signature (DS) is used to verify the authenticity and integrity of a message using a cryptographic algorithm. This can be used to validate a device’s identity to a server, or to check the integrity of a message.

ESP32-C6 includes a Digital Signature (DS) module providing hardware acceleration of messages’ signatures based on RSA. HMAC is used as the key derivation function to output the DS_KEY key using eFuse as the input key. Subsequently, the DS module uses DS_KEY to decrypt the pre-encrypted parameters and calculate the signature. The whole process happens in hardware so that neither the decryption key for the RSA parameters nor the input key for the HMAC key derivation function can be seen by users while calculating the signature.

24.2 Features

*   RSA digital signatures with key length up to 3072 bits
*   Encrypted private key data, only decryptable by DS module
*   SHA-256 digest to protect private key data against tampering by an attacker

24.3 Functional Description

24.3.1 Overview

The DS peripheral calculates RSA signatures as Z = X^Y mod M, where Z is the signature, X is the input message, and Y and M are the RSA private key parameters.

Private key parameters are stored in flash as ciphertext. They are decrypted using a key (DS_KEY) which can only be calculated by the DS peripheral via the HMAC peripheral. The required inputs (HMAC_KEY) to generate the key are only stored in eFuse and can only be accessed by the HMAC peripheral. That is to say, the DS peripheral hardware can decrypt the private key, and the private key in plaintext is never accessed by the software. For more detailed information about eFuse and HMAC peripherals, please refer to Chapter 6 eFuse Controller and 21 HMAC Accelerator (HMAC) peripheral.

The input message X will be sent directly to the DS peripheral by the software each time a signature is needed. After the RSA signature operation, the signature Z is read back by the software.

For better understanding, we define some symbols and functions here, which are only applicable to this chapter:
```