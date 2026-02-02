**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**GoBack Link:** GoBack

---

**Parameter Section Header:**

- **Parameter name:** PM, PF, DAIF, PAM, DB  
  - **Parameter setting:** 
    - Set for all except DAIF which is Cleared.

**Table Title and Description:**
Table 24.4-2 Source Address Filtering
| Frame Type | PM | SAIF | SAF | Source Address Filter Operation |
|-------------|----|------|-----|----------------------------------|
|             |     |      |     |                                   |
| 1           | X  | X    | K   | Pass all frames                   |
| 0           | O  | O    | D   | Pass when results of perfect/group filtering match. Frames not passed are not discarded. |
| Unicast      | O  | 1    |     | Fail when results of perfect/group filtering match. Frames not passed are not discarded. |
|             | O  | 0    | 1   | Pass when results of perfect/group filtering match. Frames not passed are discarded. |
|             | O  | 1    | 1   | Fail when results of perfect/group filtering match. Frames not passed are discarded. |

**Text Description:**
The filtering parameters in the MAC Frame Filter Register described in Table 24.4-2.

---

**Subsection Title and Parameter Section Header for Subsection:**  
Parameter name:
- PM
  - **Parameter setting:** Set

SAIF, Source Address Filtering (Cleared)
- SAIF: Don’t care
  
### Subsection Content:

#### Subsection Title with Numbering:
24.4.6 Good Transmitted Frames and Received Frames

**Body Text Description of Subsection:**
A frame successfully transmitted is considered a "good frame". In other words, a transmitted frame is considered to be good, if the frame transmission is not aborted due to the following errors:

- Jabber timeout
- No carrier or loss of carrier
- Late collision
- Frame underflow
- Excessive deferral
- Excessive collision

The received frames are considered "good frames", if there are not any of the following errors:
- CRC error
- Runt frames (frames shorter than 64 bytes)
- Alignment error (in 10/100 Mbps modes only)
- Length error (non-type frames only)
- Frame size over the maximum size (for non-type frames over the maximum frame size only)

**Footer:**
Espressif Systems  
Page number and document version information:
469 ESP32 TRM (Version 5.6)  

**Action Links:** Submit Documentation Feedback