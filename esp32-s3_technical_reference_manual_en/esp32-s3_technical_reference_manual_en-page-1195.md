**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Header:**
GoBack

**Body Text with Subsections and Lists:**

- **Subsection Heading:** 
  - "A Bus Off node can become the Error Active (with both its TEC and REC reset to O) after it monitors 128 occurrences of 11 consecutive recessive bits on the bus."

- **Section Title:**
  31.3.4 TWAI Bit Timing

- **Subsection Heading:** 
  - "Nominal Bit"

**Body Text with Definitions List and Figure Reference:**

The TWAI protocol allows a TWAI bus to operate at a particular bit rate. However, all nodes within a TWAI bus must operate at the same bit rate.

- The Nominal Bit Rate is defined as the number of bits transmitted per second from an ideal transmitter without any synchronization.
  
- **Note:** 
  - "The Nominal Bit Time"

A single Nominal Bit Time is divided into multiple segments, and each segment is made up of multiple Time Quanta. A Time Quantum is a fixed unit of time, and it's implemented as some form of prescaled clock signal in each node.

**Figure Reference:**
- Figure 31.3-5 illustrates the segments within a single Nominal Bit Time.
  
TWAI controllers will operate at times steps of one Time Quanta where the state of the TWAI bus is analyzed. If two consecutive Time Quantas have different states (i.e., recessive to dominant or vice versa), this will be considered an edge.

When the bus is analyzed, it's done by analyzing each intersection point between PBS1 and PBS2; these points are called Sample Points where a sampled value of that bit can occur. 

**Figure Caption:**
- "Figure 31.3-5. Layout of a Bit"

**Table Title with Table Content Description:** 
- **Table Title:** Table 31.3-5 Segments of a Nominal Bit Time

| Segment | Description |
|---------|-------------|
| SS      | The SS (Synchronization Segment) is one Time Quantum long. If all nodes are perfectly synchronized, the edge of bit will lie in the SS. |
| PBS1    | PBS1 (Phase Buffer Segment 1) can be from 1 to 16 Time Quanta long. PBS1 compensates for physical delay times within network and also lengthened synchronization purposes. |
| PBS2    | PBS2 (Phase Buffer Segment 2) is meant compensation of information processing time nodes, it's short-eneded for synchronization purpose. |

**Subsection Heading:**
31.3.4.2 Hard Synchronization and Resynchronization

**Body Text with Explanation:** 

Due to clock skew and jitter, the bit timing on a single bus may become out-of-phase due to these factors.

To ensure that internal time bits of each node are kept in sync:

- A bit edge can come before or after SS.
  
This ensures synchronization across nodes.