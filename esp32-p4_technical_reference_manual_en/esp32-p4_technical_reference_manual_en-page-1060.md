

# Chapter 15  
## System Timer  

### 15.1 Overview  

ESP32-P4 provides a 52-bit system timer, which can be used to generate tick interrupts for the operating system, or be used as a general timer to generate periodic interrupts or one-time interrupts.  

### 15.2 Features  

The system timer has the following features:  
- Two 52-bit counters and three 52-bit comparators  
- Software accessing registers clocked by APB_CLK  
- CNT_CLK used for counting, with an average frequency of 16 MHz in two counting cycles  
- 40 MHz XTAL_CLK as the clock source of CNT_CLK  
- 52-bit alarm values (t) and 26-bit alarm periods (δt)  
- Two modes to generate alarms:  
    - Target mode: only a one-time alarm is generated based on the alarm value (t)  
    - Period mode: periodic alarms are generated based on the alarm period (δt)  
- Three comparators generating three independent interrupts based on configured alarm value (t) or alarm period (δt)  
- Software configuring the reference count value. For example, the system timer is able to load back the sleep time recorded by RTC timer via software after Light-sleep  
- Able to stall or continue running when CPU stalls or enters the on-chip-debugging mode  
- Alarm for Event Task Matrix (ETM) event