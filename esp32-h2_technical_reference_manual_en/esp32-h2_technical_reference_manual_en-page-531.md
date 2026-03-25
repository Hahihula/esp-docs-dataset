

```markdown
# Chapter 16 System Registers

## 16.1 Overview

ESP32-H2 supports the following auxiliary chip features:

- External Memory Encryption/Decryption
- Anti-DPA attack security
- Bus timeout protection

Each auxiliary chip feature can be controlled with dedicated system registers. This chapter describes how to configure these system registers.

## 16.2 Function Description

### 16.2.1 External Memory Encryption/Decryption Configuration

`HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` configures encryption and decryption options of the external memory. For details about the External Memory Encryption and Decryption modules, please refer to Chapter 26 *External Memory Encryption and Decryption (XTS_AES)*.

### 16.2.2 Anti-DPA Attack Security Control

ESP32-H2 has a dual protection mechanism against Differential Power Analysis (DPA) attacks at the hardware level.

- First, a mask mechanism is introduced in the symmetric encryption operation process, which interferes with the power consumption trajectory by masking the real data in the operation process. This security mechanism cannot be turned off.
- Second, the clock selected for the operation will change dynamically in real time, blurring the power consumption trajectory during the operation. For this security mechanism, ESP32-H2 provides three security levels for users to choose to adapt to different applications.

**Table 16.2-1. Security Level**

| Security-Level Name | Value | 96M_PLL_CLK (MHz) | 64M_PLL_CLK (MHz) | XTAL_CLK (MHz) |
|---------------------|-------|-------------------|-------------------|----------------|
| SEC_DPA_OFF         | 0     | 96                | 64                | 32             |
| SEC_DPA_LOW         | 1 or 2 | (48,96)^A        | (32,64)^A         | (16,32)^A      |
| SEC_DPA_HIGH        | 3     | (32,96)^A         | (21,3,64)^A       | (10,6,32)^A    |

^A (x,y] means the operating frequency is greater than x MHz, and equal to or less than y MHz.
```