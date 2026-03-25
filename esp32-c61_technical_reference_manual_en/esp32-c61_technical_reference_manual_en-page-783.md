

```markdown
Chapter 21 SHA Accelerator (SHA)

GoBack

Chapter 21

SHA Accelerator (SHA)

21.1 Introduction

ESP32-C61 integrates an SHA accelerator, which is a hardware device that speeds up the SHA algorithm significantly, compared to a SHA algorithm implemented solely in software. The SHA accelerator integrated in ESP32-C61 has two working modes, which are Typical SHA and DMA-SHA.

21.2 Features

The following functionality is supported:

- The following hash algorithms introduced in FIPS PUB 180-4 Spec
  - SHA-1
  - SHA-224
  - SHA-256
- Two working modes
  - Typical SHA
  - DMA-SHA
- Interleaved function when working in Typical SHA working mode
- Interrupt function when working in DMA-SHA working mode

21.3 Working Modes

The SHA accelerator integrated in ESP32-C61 has two working modes.

- Typical SHA Working Mode: all the data is written and read via CPU directly.
- DMA-SHA Working Mode: all the data is read via DMA. That is, users can configure the DMA controller to read all the data needed for hash operation, thus releasing CPU for completing other tasks.

The SHA accelerator is activated by setting the PCR_SHA_CLK_EN bit and clearing the PCR_SHA_RST_EN bit in the PCR_SHA_CONF_REG register. Additionally, users also need to clear PCR_ECDSA_RST_EN bit to reset Elliptic Curve Digital Signature Algorithm (ECDSA).

Users can start the SHA accelerator with different working modes by configuring registers SHA_START_REG and SHA_DMA_START_REG. For details, please see Table 21.3-1.
```