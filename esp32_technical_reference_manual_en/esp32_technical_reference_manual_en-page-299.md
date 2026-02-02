**Title: Chapter 16 SHA Accelerator (SHA)**

**GoBack**

---

### Register 16.8. SHA_SHA256_LOAD_REG (0x098)

| Field | Description |
|-------|-------------|
| **(reserved)** | - |

- **SHA_SHA256_LOAD**: Write `1` to finish the SHA-256 operation to calculate the final message hash.
  - **Type:** (WO)
  
---

### Register 16.9. SHA_SHA256_BUY_REG (0x09C)

| Field | Description |
|-------|-------------|
| **(reserved)** | - |

- **SHA_SHA256_BUY**: SHA-256 operation status: `1` if the SHA accelerator is processing data, `0` if it is idle.
  - **Type:** (RO)
  
---

### Register 16.10. SHA_SHA384_START_REG (0x0A0)

| Field | Description |
|-------|-------------|
| **(reserved)** | - |

- **SHA_SHA384_START**: Write `1` to start an SHA-384 operation on the first message block.
  - **Type:** (WO)
  
---

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)

Submit Documentation Feedback