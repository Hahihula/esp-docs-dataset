

```markdown
Chapter 23

SHA Accelerator (SHA)

23.1 Introduction

ESP32-H2 integrates an SHA accelerator, which is a hardware device that speeds up the SHA algorithm significantly, compared to a SHA algorithm implemented solely in software. The SHA accelerator integrated in ESP32-H2 has two working modes, which are Typical SHA and DMA-SHA.

23.2 Features

The following functionality is supported:

- The following hash algorithms introduced in FIPS PUB 180-4 Spec.
  - SHA-1
  - SHA-224
  - SHA-256
- Two working modes
  - Typical SHA
  - DMA-SHA
- Interleaved function when working in Typical SHA working mode
- Interrupt function when working in DMA-SHA working mode

23.3 Working Modes

The SHA accelerator integrated in ESP32-H2 has two working modes.

- Typical SHA Working Mode: all the data is written and read via CPU directly.
- DMA-SHA Working Mode: all the data is read via DMA. That is, users can configure the DMA controller to read all the data needed for hash operation, thus releasing CPU for completing other tasks.

The SHA accelerator is activated by setting the PCR_SHA_CLK_EN bit and clearing the PCR_SHA_RST_EN bit in the PCR_SHA_CONF_REG register. Additionally, users also need to clear PCR_DS_RST_EN, PCR_HMAC_RST_EN, and PCR_ECDSA_RST_EN bits to reset Digital Signature Algorithm (DSA), HMAC Accelerator (HMAC), and Elliptic Curve Digital Signature Algorithm (ECDSA).

Users can start the SHA accelerator with different working modes by configuring registers SHA_START_REG and SHA_DMA_START_REG. For details, please see Table 23.3-1.
```