**Chapter Title:**
Chapter 18

**Section Titles and Content:**

- **SHA Accelerator (SHA)**
  - Subsection "18.1 Introduction"
    - ESP32-S3 integrates an SHA accelerator, which is a hardware device that speeds up SHA algorithm significantly compared to SHA algorithm implemented solely in software.
    - The SHA accelerator integrated in ESP32-S3 has two working modes: Typical SHA and DMA-SHA.

  - Subsection "18.2 Features"
    - Describes the supported functionality:
      - All hash algorithms introduced are specified by FIPS PUB 180-4 Spec, including:
        - SHA-1
        - SHA-224
        - SHA-256
        - SHA-384
        - SHA-512
        - SHA-512/224
        - SHA-512/256
        - SHA-512/t
      - Two working modes:
        - Typical SHA: interleaved function when in operation.
        - DMA-SHA: interrupt function used during operation.

  - Subsection "18.3 Working Modes"
    - Describes the two types of working modes for the SHA accelerator integrated into ESP32-S3, which are typical and DMA-SHA:
      - **Typical SHA Working Mode:** All data is written to and read from CPU directly.
      - **DMA-SHA Working Mode:** Data can be configured via DMA. This mode allows users to release CPU resources by having the DMA controller handle all necessary operations for hash computations.

**Footer:**
- Page number 843
- Document version ESP32-S3 TRM (Version 1.7)
- Link text "Submit Documentation Feedback"