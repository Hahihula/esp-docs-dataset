

```markdown
Chapter 30 RSA Digital Signature Peripheral (RSA_DS)

GoBack

Chapter 30

RSA Digital Signature Peripheral (RSA_DS)

30.1 Overview

The RSA Digital Signature Peripheral (RSA_DS) is used to verify the authenticity and integrity of a message using a cryptographic algorithm. This can be used to validate a device’s identity to a server or to check the integrity of a message.

ESP32-P4 includes an RSA Digital Signature Peripheral (RSA_DS) providing hardware acceleration of messages’ signatures based on RSA. HMAC is used as the key derivation function (KDF) to output the `RSA_DS_KEY` using a key stored in eFuse or deployed by the Key Manager as the input key. Subsequently, the RSA_DS peripheral uses `RSA_DS_KEY` to decrypt the pre-encrypted parameters and calculate the signature. The whole process happens in hardware so that all the keys involved during the calculating process cannot be seen by users, guaranteeing the security of the operation.

30.2 Features

*   RSA digital signatures with key length up to 4096 bits
*   Encrypted private key data, only decryptable by the RSA_DS peripheral
*   SHA-256 digest to protect private key data against tampering by an attacker

30.3 Functional Description

30.3.1 Overview

The RSA_DS peripheral calculates RSA signatures as Z = X^Y mod M, where Z is the signature, X is the input message, and Y and M are the RSA private key parameters.

Private key parameters are stored in flash as ciphertext. They are decrypted using `RSA_DS_KEY` which can:

*   Be calculated by the RSA_DS peripheral via the HMAC peripheral. The required inputs (`HMAC_KEY`) to generate the key are only stored in eFuse and can only be accessed by the HMAC peripheral. That is to say, the RSA_DS peripheral hardware can decrypt the private key, and the private key in plaintext is never accessed by the software. For more detailed information about eFuse and HMAC peripherals, please refer to Chapter 8 eFuse Controller (EFUSE) and Chapter 27 HMAC Accelerator (HMAC).
*   Deploy from Key Manager module. `RSA_DS_KEY` must be deployed by the Key Manager in a secured way.
```