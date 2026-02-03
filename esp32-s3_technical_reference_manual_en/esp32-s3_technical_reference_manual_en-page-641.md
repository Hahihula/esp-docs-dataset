**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**Section Heading:**
11.7 Registers

**Body Text:**
The addresses in this section are relative to system timer base address provided in Table 4.3-3 in Chapter 4.

**Subheading:**
System and Memory

**Register Description:**
Register 11.1. SYSTIMER_CONF_REG (0x0000)

**Binary Diagram with Labels for Each Bit:**
```
+-----------------------------+
| 31 | 30 | 29 | ... | 26 | 25 | 24 | 23 | 22 | 21 | (reserved) |
+-------------+-------------+-------------+-------------+-------------+-------------+-------------+-------------+-------------+-------------+
| O   |    |     |      |       |        |         |           |            |             |
+-------------+-------------+-------------+-------------+-------------+-------------+-------------+-------------+-------------+-------------+
```

**Bit Labels and Descriptions:**
- SYSTIMER_CLK_EN
  - Register clock gating. 
  - 1: Register clock is always enabled for read and write operations.
  - 0: Only enable needed clock for register read or write operations.

- SYSTIMER_TARGET2_WORK_EN, SYSTIMER_TARGET1_WORK_EN, SYSTIMER_TARGETO_WORK_EN:
  - COMP2 work enable bit. (R/W)
  - COMP1 work enable bit. (R/W)
  - COMPO work enable bit. (R/W)

- SYSTIMER_TIMER_UNIT1_CORE0_STALL_EN
  - UNIT1 is stalled when CPU1 stalled.
  - (R/W)

- SYSTIMER_TIMER_UNIT1_COREO_STALL_EN, SYSTIMER_TIMER_UNIT1_STALL_EN:
  - UNIT1 is stalled when CPU0 stalled. 
  - (R/W)

- SYSTIMER_TIMER_UNIT1Unit0_STALL_EN
  - UNIT0 is stalled when CU1 stalled.
  - (R/W)

- SYSTIMER_TIMER_UNIT1Unit0_STALL_EN, SYSTIMER_TIMER_UNIT1Unit0_STALL_EN:
  - UNIT0 is stalled when CPU0 stalled. 
  - (R/W)

**Footer:**
Espressif Systems
641 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback