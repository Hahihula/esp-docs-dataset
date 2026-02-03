**Chapter Title:**
Chapter 22

**Section Heading: Digital Signature (DS)**

**Subsection 22.1 Overview**

A Digital Signature is used to verify the authenticity and integrity of a message using a cryptographic algorithm.
This can be used to validate a device’s identity to a server, or to check the integrity of a message.

The ESP32-S3 includes a Digital Signature (DS) module providing hardware acceleration of messages’ signatures based on RSA. It uses pre-encrypted parameters to calculate a signature. The parameters are encrypted using HMAC as a key-derivation function. In turn, the HMAC uses Fuses as an input key. The whole process happens in hardware so that neither the decryption key for the RSA parameters nor the input key for the HMAC key derivation function can be seen by the users while calculating the signature.

**Subsection 22.2 Features**

- RSA Digital Signatures with key length up to 4096 bits
- Encrypted private key data, only decryptable by DS peripheral
- SHA-256 digest to protect private key data against tampering by an attacker

**Section Heading: Functional Description (Subsection 22.3)**

**Subsection 22.3.1 Overview**

The DS peripheral calculates RSA a signature as \( Z = X^Y \mod M \) where \( Z \) is the signature, \( X \) is the input message, and \( Y \) are the RSA private key parameters.

Private key parameters are stored in flash or other memory as ciphertext. They are decrypted using a key (DS_KEY) which can only be read by the DS peripheral via the HMAC peripheral. The required inputs (HMAC_KEY) to generate the key are only stored in eFuse and can only be accessed by the HMAC peripheral. The DS peripheral hardware can decrypt the private key, and the private key in plaintext is never accessed by the software.

For more detailed information about eFuse and HMAC peripherals, please refer to Chapter 5 eFuse Controller and HMAc Accelerator (HMAC) peripheral.

The input message \( X \) will be sent directly to the DS peripheral by the software, each time a signature is needed. After the RSA signature operation, the signature \( Z \) read back by the software.
For better understanding, we define some symbols and functions here, which are only applicable to this chapter:
- 1^: A bit string consist of s bits that stores “1”.

**Footer Information**
Espressif Systems
898 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback