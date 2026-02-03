**Chapter Title:**
Chapter 23

**Section Heading:**
External Memory Encryption and Decryption (XTS_AES)

**Subsection 23.1 - Overview**

The ESP32-S3 integrates an External Memory Encryption and Decryption module that complies with the XTS_AES standard algorithm specified in IEEE Std 1619-2007, providing security for users' application code and data stored in the external memory (flash and RAM). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) to the external flash, or store general data to the external RAM.

**Subsection 23.2 - Features**

- General XTS_AES algorithm, compliant with IEEE Std 1619-2007
- Software-based manual encryption
- High-speed auto encryption, without software's participation
- High-speed auto decryption, without software’s participation
- Encryption and decryption functions jointly determined by registers configuration, eFuse parameters, and boot mode

**Subsection 23.3 - Module Structure**

The External Memory Encryption and Decryption module consists of three blocks, namely the Manual Encryption block, Auto Encryption block, and Auto Decryption block. The module architecture is shown in Figure 23.3-1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 
908 ESP32-S3 TRM (Version 1.7)