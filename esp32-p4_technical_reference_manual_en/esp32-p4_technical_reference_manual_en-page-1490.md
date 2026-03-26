

```markdown
Chapter 29

SHA Accelerator (SHA)

29.1 Introduction

ESP32-P4 integrates an SHA accelerator, which is a hardware device that speeds up the SHA algorithm significantly, compared to an SHA algorithm implemented solely in software. The SHA accelerator integrated in ESP32-P4 has two working modes, which are Typical SHA and DMA-SHA.

29.2 Features

The following functionality is supported:

- The following hash algorithms introduced in FIPS PUB 180-4 Spec.
  - SHA-1
  - SHA-224
  - SHA-256
  - SHA-384
  - SHA-512
  - SHA-512/224
  - SHA-512/256
  - SHA-512/t

- Two working modes
  - Typical SHA
  - DMA-SHA

- Interleaved function when working in Typical SHA working mode
- Interrupt function when working in DMA-SHA working mode

29.3 Working Modes

The SHA accelerator integrated in ESP32-P4 has two working modes.

- Typical SHA Working Mode: all the data is written and read via CPU directly.
- DMA-SHA Working Mode: all the data is read via DMA. That is, users can configure the GDMA-AXI controller to read all the data needed for hash operation, thus releasing CPU for completing other tasks.
```