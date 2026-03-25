

```markdown
Chapter 15  
RTC Timer  

15.1 Introduction  

The RTC Timer is a 48-bit readable counter that can operate in any power mode. It is used as a system timer when the timers in the HP system is unavailable. It also allows for configuring timer interrupts and logging the time when specific events happen in the system.  

15.2 Feature List  

- 48-bit counter  
- Time logging when one of the following events happens:  
    - HP system reset  
    - CPU enters stall state  
    - CPU exits stall state  
    - Crystal powers up  
    - Crystal powers down  
- Time logging through register configuration  
- Occurrence time cached of the most recent two specific events  
- Generation of interrupts at the target time, which is configurable  
- Uninterrupted operation during any reset or sleep mode, except for power-on reset of LP system  
- Can work as the wake-up source (see Chapter 11 Low-Power Management)  

15.3 Functional Description  

- 48-bit counter  
    - The implementation of the RTC Timer is based on a 48-bit counter, driven by the RC_SLOW_CLK in the Always-On power domain (for details about power domains, see Chapter 11 Low-Power Management). It uses continuous loop counting (except during LP system reset), and an overflow interrupt is generated when the 48-bit counter overflows.  
- Log the occurrence time of specific events  
    - The RTC Timer supports logging the occurrence time of three types of events:
```