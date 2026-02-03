**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Body Text with Subheadings and Lists:**

- **Register locks to secure the integrity of Permission Control related registers**
- Protection to secure the integrity of CPU’s VECBASE registers

---

**Subheading:** 
15.3 Internal Memory

**Body Text:**
ESP32-S3 has the following types of internal memory:

- ROM: 384 KB in total, including 256 KB Internal ROM0 and 128 KB Internal ROM1
- SRAM: 512 KB in total, including 32 KB Internal SRAM0, 416 KB Internal SRAM1, and 64 KB Internal SRAM2
- RTC FAST Memory: 8 KB in total, which can be split into two regions with independent permission configuration
- RTC SLOW Memory: 8 KB in total, which can further be split into two regions each with independent permission configuration

This section describes how to configure the permission to each types of ESP32-S3’s internal memory.

---

**Subheading:** 
15.3.1 ROM

**Body Text:**
ESP32-S3's ROM can be accessed by CPU’s instruction bus (IBUS) and data bus (DBUS) when configured.
Note:
- Permission for Secure World and Non-secure World can be configured independently.

Once configured, the permission applies to both CPU0 and CPU1

---

**Subheading:** 
15.3.1.1 Address

**Body Text:**
ESP32-S3’s ROM address and the address ranges accessible for IBUS and DBUS respectively are listed in Table 15.3-1.

**Table Title (with headers):**
Table 15.3-1. ROM Address
| ROM | IBUS Address | Starting Address | Ending Address | Starting Address | Ending Address |
|---|---|---|---|---|---|
| Internal ROM0 | - | Ox4000_0000 | FFFF | - | _ |
| Internal ROM1 | 0x4004_0000 | 0x4005_FFFF | FFFE | 0x3FF0_0000 | 0x3FF1_FFFF |

---

**Subheading:** 
15.3.1.2 Access Configuration

**Body Text:**
ESP32-S3 uses the registers listed in Table 15.3-2 to configure the instruction execution (X), write (W) and read (R) accesses of CPU’s IBUS and DBUS, from the Secure World and Non-secure World, to ROM:

---

**Footer Information:** 
Espressif Systems
684 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback