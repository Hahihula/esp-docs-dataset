**Title:**
Chapter 30 SPI Controller (SPI)

**Diagram Title and Description:**
Figure 30.8-1. Timing Compensation Control Diagram in GP-SPI2 Master Mode

**Body Text with Descriptions of Key Components on the Diagrams:**

- **Key Registers:**
  - `SPI_DIN_MODE_REG`: select the latch edge of input data
  - `SPI_NUM_REG`: select the delay cycles of input data
  - `SPI_OUT_MODE_REG`: select the latch edge of output data

**Subsection Title and Description:**
Timing Compensation Example

**Additional Information in Body Text:**

Figure 30.8-2 shows a timing compensation example in GP-SPI2 master mode. Note that DUMMY cycle length is configurable to compensate the delay in I/O lines, so as to enhance the performance of GP-SPI2.

**Footer with Document Information and Navigation Links:**
Espressif Systems
1146 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Navigation Link at Top Right Corner:** GoBack