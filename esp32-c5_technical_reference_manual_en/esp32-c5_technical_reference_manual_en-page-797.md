

# Chapter 19 System Registers

## 19.1 Overview

ESP32-C5 supports a set of auxiliary chip features listed in subsection 19.2 Features below. This chapter describes the registers used to configure these features.

## 19.2 Features

ESP32-C5 system registers control the following peripheral blocks and core modules:

- External Memory Encryption/Decryption
- Anti-DPA attack security
- HP CPU/LP CPU debug
- Bus timeout protection

## 19.3 Function Description

### 19.3.1 External Memory Encryption/Decryption Configuration

Register `HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` configures encryption and decryption options of the external memory. For details, please refer to Chapter 29 *External Memory Encryption and Decryption (XTS_AES)*.

### 19.3.2 Anti-DPA Attack Security Control

ESP32-C5 has a dual protection mechanism against Differential Power Analysis (DPA) attacks at the hardware level.

- First, a mask mechanism is introduced in the symmetric encryption operation, which interferes with the power consumption trajectory by masking the real data in the operation process. This security mechanism cannot be turned off.
- Second, the clock selected for the operation will change dynamically in real time, blurring the power consumption trajectory during the operation. For this security mechanism, ESP32-C5 provides 4 security levels for users to choose to adapt to different applications.