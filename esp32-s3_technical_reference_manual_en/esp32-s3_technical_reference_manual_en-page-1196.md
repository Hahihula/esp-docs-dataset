**Title: Chapter 31 Two-wire Automotive Interface (TWAI®)**

**Body Text:**
In phase, TWAI has various methods of synchronization. The Phase Error “e” is measured in the number of Time Quanta and relative to the SS.

- A positive Phase Error (e > 0) when the edge lies after the SS and before the Sample Point (i.e., the edge is late).
- A negative Phase Error (e < 0) is when the edge lies after the Sample Point of the previous bit and before SS (i.e., the edge is early).

To correct for Phase Errors, there are two forms of synchronization, known as Hard Synchronization and Resynchronization. **Hard Synchronization** and **Resynchronization** obey the following rules:

- Only one synchronization may occur in a single bit time.
- Synchronizations only occurs on recessive to dominant edges.

**Subtitle: 31.4 Architectural Overview**

**Body Text under Subtitle:**
The major functional blocks of the TWAI controller are shown in Figure **31.4-1**:

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:** 
ESP32-S3 TRM (Version 1.7)