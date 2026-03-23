

```markdown
Glossary

Most frequently used access types and their combinations are as follows:

* RO
* WO
* WT
* R/W
* R/W1
* WL
* R/W/SC

* R/W/SS
* R/W/SS/SC
* R/WC/SS
* R/WC/SC
* R/WC/SS/SC
* R/WS/SC
* R/WS/SS

* R/WS/SS/SC
* R/SS/WTC
* R/SC/WTC
* R/SS/SC/WTC
* RF/WF
* R/SS/RC
* varies

Descriptions of all access types are provided below.

R   Read. User application can read from this register/field; usually combined with other access types.
RO  Read only. User application can only read from this register/field.
HRO Hardware Read Only. Only hardware can read from this register/field; used for storing default settings for variable parameters.
W   Write. User application can write to this register/field; usually combined with other access types.
WO  Write only. User application can only write to this register/field.
W1  Write Once. User application can write to this register/field only once; only allowed to write 1; writing 0 is invalid.
SS  Self set. On a specified event, hardware automatically writes 1 to this register/field; used with 1-bit fields.
SC  Self clear. On a specified event, hardware automatically writes 0 to this register/field; used with 1-bit and multi-bit fields.
SM  Self modify. On a specified event, hardware automatically writes a specified value to this register/field; used with multi-bit fields.
SU  Self update. On a specified event, hardware automatically updates this register/field; used with multi-bit fields.
RS  Read to set. If user application reads from this register/field, hardware automatically writes 1 to it.
RC  Read to clear. If user application reads from this register/field, hardware automatically writes 0 to it.
RF  Read from FIFO. If user application writes new data to FIFO, the register/field automatically reads it.
WF  Write to FIFO. If user application writes new data to this register/field, it automatically passes the data to FIFO via APB bus.
WS  Write any value to set. If user application writes to this register/field, hardware automatically sets this register/field.
W1S Write 1 to set. If user application writes 1 to this register/field, hardware automatically sets this register/field.
WOS Write 0 to set. If user application writes 0 to this register/field, hardware automatically sets this register/field.

GoBack

Espressif Systems
893
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```