

# Chapter 25 ## External Memory Encryption and Decryption (XTS_AES)

### 25.1 Overview

The ESP32-C6 integrates an External Memory Encryption and Decryption module that complies with the XTS-AES standard algorithm specified in IEEE Std 1619-2007, providing security for users’ application code and data stored in the external memory (flash). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) to the external flash.

### 25.2 Features

* General XTS-AES algorithm, compliant with IEEE Std 1619-2007
* Software-based manual encryption
* High-speed auto decryption without software’s participation
* Encryption and decryption functions jointly enabled/disabled by registers configuration, eFuse parameters, and boot mode
* Configurable Anti-DPA

### 25.3 Module Structure

The External Memory Encryption and Decryption module consists of two blocks, namely the Manual Encryption block and Auto Decryption block. The module architecture is shown in Figure 25.3-1.