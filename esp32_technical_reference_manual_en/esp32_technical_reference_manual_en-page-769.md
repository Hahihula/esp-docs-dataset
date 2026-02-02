**Title: Glossary**

- **W1S**: Write 1 to set. If user application writes 1 to this register/field, hardware automatically sets this register/field.
  
- **WOS**: Write O to set. If user application writes 0 to this register/field, hardware automatically sets this register/field.

- **WC**: Write any value to clear. If user application writes to this register/field, hardware automatically clears this register/field.

- **W1C**: Write 1 to clear. If user application writes 1 to this register/field, hardware automatically clears this register/field.

- **WOC**: Write O to clear. If user application writes 0 to this register/field, hardware automatically clears this register/field.

- **WT**: Write 1 to trigger an event. If user application writes 1 to this field, this action triggers an event (pulse in the APB bus) or clears a corresponding WTC field (see WTC).

- **WTC**: Write to clear. Hardware automatically clears this field if user application writes 1 to the corresponding WT field (see WT).

- **WTI**: Write I to toggle. If user application writes I to this field, hardware automatically inverts the corresponding field; otherwise - no effect.

- **WOT**: Write O to toggle. If user application writes O to this field, hardware automatically inverts the corresponding field; otherwise - no effect.

- **WL**: Write if a lock is deactivated. If the lock is deactivated, user application can write to this register/field.

**Note:** The access type varies. Different fields of this register might have different access types.

---

Espressif Systems  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)