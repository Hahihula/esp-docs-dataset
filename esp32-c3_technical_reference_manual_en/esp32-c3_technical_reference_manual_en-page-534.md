

```markdown
# Chapter 23

## External Memory Encryption and Decryption (XTS_AES)

### 23.1 Overview

The ESP32-C3 integrates an External Memory Encryption and Decryption module that complies with the XTS_AES standard algorithm specified in [IEEE Std 1619-2007](#), providing security for users’ application code and data stored in the external memory (flash). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) to the external flash.

### 23.2 Features

* General XTS_AES algorithm, compliant with IEEE Std 1619-2007
* Software-based manual encryption
* High-speed auto decryption, without software’s participation
* Encryption and decryption functions jointly determined by registers configuration, eFuse parameters, and boot mode

### 23.3 Module Structure

The External Memory Encryption and Decryption module consists of two blocks, namely the Manual Encryption block and Auto Decryption block. The module architecture is shown in Figure 23.3-1.
```