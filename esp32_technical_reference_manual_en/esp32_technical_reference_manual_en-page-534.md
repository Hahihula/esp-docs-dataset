**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** [GoBack](#)

---

**Table:**

| Segment | Description |
|---------|-------------|
| PBS1    | PBS1 (Phase Buffer Segment 1) can be 1 to 16 Time Quanta long. PBS1 is meant to compensate for the physical delay times within the network. PBS1 can also be lengthened for synchronization purposes. |
| PBS2    | PBS2 (Phase Buffer Segment 2) can be 1 to 8 Time Quanta long. PBS2 is meant to compensate for the information processing time of nodes. PBS2 can also be shortened for synchronization purposes. |

---

**Section Title:**
25.3.4.2 Hard Synchronization and Resynchronization

**Body Text:**

Due to clock skew and jitter, the bit timing of nodes on the same bus may become out of phase. Therefore, a bit edge may come before or after the SS. To ensure that the internal bit timing clocks of each node are kept in phase, TWAI has various methods of synchronization. The Phase Error “e” is measured in the number of Time Quanta relative to the SS.

- A positive Phase Error (e > 0) is when the edge lies after the SS and before the Sample Point (i.e., the edge is late).
- A negative Phase Error (e < 0) is when the edge lies after the Sample Point of the previous bit and before SS (i.e., the edge is early).

To correct for Phase Errors, there are two forms of synchronization, known as Hard Synchronization and Resynchronization. Hard Synchronization and Resynchronization obey the following rules:

- Only one synchronization may occur in a single bit time.
- Synchronizations only occurs on Recessive to Dominant edges.

**Subsection Title:**
Hard Synchronization

**Body Text:**

Hard Synchronization occurs on the Recessive to Dominant edges during Bus Idle (i.e., the SOF bit). All nodes will restart their internal bit timings such that the Recessive to Dominant edge lies within the SS of the restarted bit timing.

**Subsection Title:**
Resynchronization

**Body Text:**

Resynchronization occurs on Recessive to Dominant edges not during Bus Idle. If the edge has a positive Phase Error (e > 0), PBS1 is lengthened by a certain number of Time Quanta. If the edge has a negative Phase Error (e < 0), PBS2 will be shortened by a certain number of Time Quanta.

The number of Time Quanta to lengthen or shorten depends on the magnitude of the Phase Error, and is also limited by the Synchronization Jump Width (SJW) value which is a programmable:

- When the magnitude of the Phase Error is less than or equal to the SJW, PBS1/PBS2 are lengthened/shortened by number of Time Quanta. This has a same effect as Hard Synchronization.
- When the magnitude of the Phase Error is greater to the SJW, PBS1/PBS2 are lengthened/shortened by the SJW number of Time Quanta. This means it may take multiple bits of synchronization before the Phase Error is entirely corrected.

---

**Section Title:**
25.4 Architectural Overview

**Body Text:**

The ESP32 contains a TWAI Controller. Figure 25.4-1 shows the major functional blocks of the TWAI Controller.

**Footer Information:**  
Espressif Systems  
Page Number: 534  
Document Version (Version 5.6)  

[Submit Documentation Feedback](#)