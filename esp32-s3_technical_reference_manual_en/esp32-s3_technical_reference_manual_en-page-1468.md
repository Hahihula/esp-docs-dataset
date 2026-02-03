**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** (Located at top right corner)

**Body Text with List Items:**

- **Timer**: the dedicated timer for DIG ADC1 controller, to initiate a sampling enable signal.
  
- **DIG ADC FSM1**: is used to
  - receive the sampling enable signal from the timer.
  - generate ADC configuration according to the pattern table.

- drive the Digital Reader1 module to read ADC sampling value. 
- transfer the sampling value to the filter, and then to memory.

- **Filter**: the filter0/1 will automatically filter the sampled ADC data for the configured channel.

- **Threshold Monitor**: the monitor0/1 will trigger a interrupt when the sampled value is greater than the pre-set high threshold or less than the pre-set low threshold.
  
- Mode control (MODE CNTL): filter the sampling signals triggered by the timer, supporting single SAR-ADC sampling. 

  - Digital Reader1 (driven by DIG ADC FSM1): reads data from SAR ADC1.

  - RTC Controller1/2: provides sampling enable signal, drives the RTC Reader1/2 to read the sampling values from ADC, then stores the sampling data to memory.
  
  - RTC Reader1/2 (driven by RTC Controller1/2): reads data from SAR ADC1/2.

**Subsection Title and Description with Table Reference:**
39.3.4 Input Signals

In order to sample an analog signal, an SAR ADC must first select the analog pin to measure via an internal multiplexer. A summary of all the analog signals that may be sent to the SAR ADC1 or SAR ADC2 for processing are presented in Table 39.3-1.

**Table Title and Content:**
Table 39.3-1. SAR ADC Input Signals

| Pin/Signal | Channel | ADC Selection |
|-------------|---------|---------------|
| GPIO1       | 0       | SAR ADC1     |
| GPIO2       | 1       |               |
| GPIO3       | 2       |               |
| GPIO4       | 3       |               |
| GPIO5       | 4       |               |
| GPIO6       | 5       |               |
| GPIO7       | 6       |               |
| GPIO8       | 7       |               |
| GPIO9       | 8       |               |
| GPIO10      | 9       |               |
| GPIO11      | 0       | SAR ADC2     |
| GPIO12      | 1       |               |
| GPIO13      | 2       |               |
| GPIO14      | 3       |               |
| GPIO15      | 4       |               |
| GPIO16      | 5       |               |
| GPIO17      | 6       |               |

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)