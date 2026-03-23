

# Chapter 21

## SHA Accelerator (SHA)

### 21.1 Introduction

ESP32-C3 integrates an SHA accelerator, which is a hardware device that speeds up SHA algorithm significantly, compared to SHA algorithm implemented solely in software. The SHA accelerator integrated in ESP32-C3 has two working modes, which are **Typical SHA** and **DMA-SHA**.

### 21.2 Features

The following functionality is supported:

- The following hash algorithms introduced in [FIPS PUB 180-4 Spec](#)
  - SHA-1
  - SHA-224
  - SHA-256
- Two working modes
  - Typical SHA
  - DMA-SHA
- Interleaved function when working in Typical SHA working mode
- Interrupt function when working in DMA-SHA working mode

### 21.3 Working Modes

The SHA accelerator integrated in ESP32-C3 has two working modes.

- **Typical SHA Working Mode**: all the data is written and read via CPU directly.
- **DMA-SHA Working Mode**: all the data is read via DMA. That is, users can configure the DMA controller to read all the data needed for hash operation, thus releasing CPU for completing other tasks.

Users can start the SHA accelerator with different working modes by configuring registers `SHA_START_REG` and `SHA_DMA_START_REG`. For details, please see Table 21.3-1.

**Table 21.3-1. SHA Accelerator Working Mode**

| Working Mode | Configuration Method |
|--------------|----------------------|
| Typical SHA  | Set SHA_START_REG to 1 |

Espressif Systems
513
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback