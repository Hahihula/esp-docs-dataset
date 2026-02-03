**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Body Text:**

The TWAI controller Acceptance Filter allows the 32-bit Acceptance Code and Mask Values to either define a single filter (i.e., Single Filter Mode), or two filters (i.e., Dual Filter Mode). How the Acceptance Filter interprets the 32-bit code and mask values is dependent on whether Single Filter Mode is enabled, and the received message format (i.e., SFF or EFF).

**Subtitle:**
31.5.6.1 Single Filter Mode

**Body Text under Subtitle:**

Single Filter Mode is enabled by setting the TWAI_RX_FILTER_MODE bit to 1. This will cause the 32-bit code and mask values to define a single filter. The single filter can filter the following bits of a data or remote frame:

- SFF
  - The entire 11-bit ID
  - RTR bit

- Data byte 1 and Data byte 2

- EFF
  - The entire 29-bit ID
  - RTR bit

The following Figure **31.5-2** illustrates how the 32-bit code and mask values will be interpreted under Single Filter Mode.

**Figure Caption:**
Figure 31.5-2. Single Filter Mode

**Table in Image (not transcribed due to complexity)**

**Subtitle:**
31.5.6.2 Dual Filter Mode

**Body Text under Subtitle:**

Dual Filter Mode is enabled by clearing the TWAI_RX_FILTER_MODE bit to 0. This will cause the 32-bit code and mask values to define a two separate filters referred to as filter 1 or filter 2. Under Dual Filter Mode, a message will be accepted if it is accepted by one of the two filters.

The two filters can filter the following bits of a data or remote frame:

- SFF

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)