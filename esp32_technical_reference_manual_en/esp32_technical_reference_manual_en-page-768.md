**Title: Access Types for Registers**

**Body Text:**
Sections Register Summary and Register Description in TRM chapters specify access types for registers and their fields.

Most frequently used access types and their combinations are as follows:

- RO
  - R/W/SS
  - R/WS/SS/SC
  - WO
  - R/W/SS/SC
  - R/SS/WTC
  - WT
  - R/WC/SS
  - R/SC/WTC
  - RW
  - R/WC/SC
  - PSSC/WTC
  - RW1
  - RF/WF
  - WL
  - R/WS/SC
  - RS/RC

- **R/W/SC**
  - varies (Note: This point is marked with a bullet, indicating it might be an additional note or variation)

**Subsection Title: Descriptions of all access types provided below.**

- `R` Read.
  - User application can read from this register/field; usually combined with other access types.

- `RO` Read only.
  - User application can only read from this register/field.

- `HRO` Hardware Read Only.
  - Only hardware can read from this register/field; used for storing default settings for variable parameters.

- `W` Write.
  - User application can write to this register/field; usually combined with other access types.

- `WO` Write only.
  - User application can only write to this register/field.

- `W1` Write Once.
  - User application can write to this register/field, but it is allowed once and writing again will be invalid (only used for registers that are not meant to change).

- `SS` Self set.
  - On a specified event, hardware automatically writes 1s to the register/field; usually combined with multi-bit fields.

- `SC` Self clear.
  - On a specified event, hardware automatically clears all bits in this field (usually used for registers that are not meant to change).

- `SM` Self modify.
  - On a specified event, hardware writes specific values or updates the register/field; usually combined with multi-bit fields.

- `SU` Self update.
  - On a specified event, hardware automatically updates all bits in this field (usually used for registers that are not meant to change).

- `RS` Read to set.
  - If user application reads from this register/field, the value is written back into it; usually combined with multi-bit fields.

- `RC` Read to clear.
  - If user application writes a specific bit in this field (usually used for registers that are not meant to change).

- `RF` Read from FIFO.
  - User can read data automatically if new data has been added by the hardware or software; usually combined with multi-bit fields.

- `WF` Write to FIFO.
  - If user application writes a specific bit in this field, it is written back into the FIFO (usually used for registers that are not meant to change).

- `WS` Write any value set.
  - User can write data automatically if new data has been added by hardware or software; usually combined with multi-bit fields.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
768

[Submit Documentation Feedback](#)