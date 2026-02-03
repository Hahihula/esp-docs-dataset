**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Body Text:**

The sampled value (result of the measurement) is the value of the touch counter, and is referred to as “touch_raw_data”. “touch_raw_data” can be read from SENS_TOUCH_PADn_DATA. However, depending on the configuration of SENS TOUCH DATA SEL, the value returned by SENS TOUCH PADn DATA could also be filtered versions of "touch_raw_data" (namely touch_smooth_data and benchmark). See section 39.2.7 for details regarding the various types of sample values, and how they are used to detect a touch.

Note: If the pulse counter does not reach its count threshold after a prolonged period of time, the touch counter will reach the timeout threshold set in RTC_CNTL_TOUCH_TIMEOUT_NUM. This will trigger a TOUCH_TIME_OUT_INT timeout interrupt and indicates a circuit exception. If TOUCH Timeout is enabled as a wake-up source from sleep modes, a wake-up signal will also be triggered (refer to Section 10.4.4 for more information).

**Subsection Title:**
39.2.6.2 Measurement Trigger Source

The Touch FSM initiates a measurement by sending a “START” signal. This “START” signal can either be triggered by software, or by a dedicated hardware timer known as the "touch timer". Using the touch timer allows for measurements to be conducted periodically without software intervention.

The touch timer is clocked by RTC_SLOW_CLK and should be configured with a period (in number of RTC_SLOW_CLK cycles). The “START” signal will be generated when the touch timer expires. When the measurement completes, the touch timer will reset and begin counting towards the next expiry time.

- To configure the "START" signal to be triggered by software:
  - Set RTC_CNTL_TOUCH_START FORCE.
  - Once configured, setting RTC_CNTL_TOUCH START EN by software will generate the “START” signal to initiate a measurement.
  
- To configure the “START” signal to be triggered by the touch timer:
  - Clear RTC_CNTL TOUCH START FORCE.
  - Configure the touch timer’s period (in RTC_SLOW_CLK) cycles in RTC_CNTL TOUCH SLEEP CYCLES.
  - Set RTC_CNTL TOUCH SLP_TIMER EN to enable the touch timer.

**Subsection Title:**
39.2.6.3 Scan Mode

Scan mode involves the Touch FSM taking measurements of multiple touch sensors in sequential order. On every “START” signal, a new touch sensor is selected for measurement, thus allowing multiple touch pins to be monitored. The scan process is illustrated in Figure 39.2-5.

**Footer:**
Espressif Systems
1460 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback