**Chapter Title:**
Chapter 5 eFuse Controller

**Navigation Link:**
GoBack

**Body Text with Table Reference and Description:**
Table 5.3-2 lists all key purpose and their values. Setting the eFuse parameter EFUSE_KEY PURPOSE_n declares the purpose of KEYn (m : 0 ~ 5).

**Table Title:**
Table 5.3-2. Secure Key Purpose Values

**Table Headers:**
Key | Purpose
---|---
Values | Purposes

**Table Content:**
1. User purposes  
2. Reserved  
3. XTS_AES_256_KEY_1 (flash/SRAM encryption and decryption)  
4. XTS_AES_256_KEY_2 (flash/SRAM encryption and decryption)  
5. HMAC Downstream mode  
6. JTAG in HMAC Downstream mode  
7. Digital Signature peripheral in HMAC Downstream mode  
8. HMAC Upstream mode  
9. SECURE_BOOT_DIGEST0 (secure boot key digest)  
10. SECURE_BOOT_DIGEST1 (secure boot key digest)  
11. SECURE_BOOT_DIGEST2 (secure boot key digest)

**Additional Information:**
Table 5.3-3 provides the details of parameters in BLOCK1 ~ BLOCK10.

**Footer Text and Navigation Links:**
Espressif Systems
Submit Documentation Feedback

**Document Version Note at Bottom Right Corner:**
ESP32-S3 TRM (Version 1.7)