**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Body Text:**
Each filtered bit of the message must either match the acceptance code or be masked in order for the message to be accepted, as demonstrated in Figure **25.5-1**.

The TWAI Controller Acceptance Filter allows the 32-bit Code and Mask values to either define a single filter (i.e., Single Filter Mode), or two filters (i.e., Dual Filter Mode). How the Acceptance Filter interprets the 32-bit code and mask values is dependent on whether Single Filter Mode is enabled, and the received message (i.e., SFF or EFF).

**Figure Caption:**
Figure **25.5-1**: Acceptance Filter

**Diagram Description in Text Format:**
```
message bit
       |
XNOR         OR         AND
       acceptance code bit  acceptance mask bit
       -------------------
                           1 = accepted
                           0 = not accepted
```

**Subsection Title and Subheading with Content:**

**25.5.6.1 Single Filter Mode**
Single Filter Mode is enabled by setting the **TWAI_RX_FILTER_MODE** bit to 1. This will cause the 32-bit code and mask values to define a single filter. The single filter can filter the following bits of a Data or Remote Frame:

- SFF
  - The entire 11-bit ID
  - RTR bit

  - Data byte 1 and Data byte 2

- EFF
  - The entire 29-bit ID
  - RTR bit

The following Figure **25.5-2** illustrates how the 32-bit code and mask values will be interpreted under Single Filter Mode.

**Figure Caption:**
Figure **25.5-2**: Single Filter Mode

**Table Description in Text Format (from Table Image):**

| ID = Identifier | ACR = TWAI_ACCEPTANCE_CODE | AMR = TWAI ACCEPTANCE_MASK |
|------------------|----------------------------|-----------------------------|
| DB = Data Byte  |                             |                            |
|                  |                             |                            |

- **ACRO – Addr 0x0040**
  - 7,6,5,4,3,2,1,0

- **AMR0 – Addr 0x0050**
  - 7,6,5,4,3,2,1,0

- **ACR1 – Addr 0x0044**
  - 7,6,5,4,3,2,1,0

- **AMR1 – Addr 0x0054**
  - 7,6,5,4,3,2,1,0

- **ACR2 – Addr 0x0048**
  - 7,6,5,4,3,2,1,0

- **AMR2 – Addr 0x0058**
  - 7,6,5,4,3,2,1,0

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32 TRM (Version 5.6)