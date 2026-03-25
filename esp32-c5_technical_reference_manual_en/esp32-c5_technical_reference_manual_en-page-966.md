

```markdown
# Chapter 29

## External Memory Encryption and Decryption (XTS_AES)

### 29.1 Overview

The ESP32-C5 integrates an External Memory Encryption and Decryption module that complies with the XTS-AES standard algorithm specified in IEEE Std 1619-2007, providing security for users’ application code and data stored in the external memory (flash and RAM). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) in the external flash, or store general data in the external RAM.

### 29.2 Features

• General XTS-AES algorithm, compliant with IEEE Std 1619-2007  
• Software-based manual encryption  
• High-speed auto encryption and decryption without software’s participation  
• Encryption and decryption functions jointly enabled/disabled by registers configuration, eFuse parameters, and boot mode  
• Configurable Anti-DPA  

### 29.3 Module Structure

The External Memory Encryption and Decryption module consists of three blocks, namely the Manual Encryption block, Auto Encryption block and Auto Decryption block. The module architecture is shown in Figure 29.3-1.
```