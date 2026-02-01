**Title: Functional Description**

---

### Feature List

- **16 KB of L1 instruction cache, 64 B of block size, four-way set associative**
- **64 KB of L1 data cache, 64 B of block size, two-way set associative, supporting two writing strategies write-through and write-back**
- **128 KB/256 KB/512 KB of L2 cache, 64 B/128 B of block size, eight-way set associative**
- **Cacheable and non-cacheable access**
- **Pre-load function**
- **Lock function**
- **Critical word first and early restart**

---

### Section: System Components

**Subtitle:** 4.1.4

This subsection describes the essential components that contribute to the overall functionality and control of the system.

---

### Subsection: GPIO Matrix and IO MUX (4.1.4.1)

The ESP32-P4 chip features 55 GPIO pins, including 16 low-power (LP) GPIO pins and 39 high-performance (HP) GPIO pins. Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal.

- **Through HP GPIO matrix and HP IO MUX:** HP peripheral input signals can be from any GPIO pins, and HP peripheral output signals can be routed to any GPIO pins.
- **Through LP GPIO matrix and LP IO MUX:** LP peripheral input signals can be from any LP GPIO pins, and LP peripheral output signals can be routed to any LP GPIO pins.

Together these modules provide highly configurable I/O. The 55 GPIO pins are numbered from GPIO0 to GPIO54:
- **LP GPIO pins (GPIO0 - GPIO15)**: Can be used by either HP or LP peripherals.
- **HP GPIO pins (GPIO16 - GPIO54)**: Can be used only by HP peripherals.

---

### Feature List

**Subtitle:** HP GPIO matrix has the following features:

- A full-switching matrix between HP peripheral input/output signals and the GPIO pins
- 222 HP peripheral input signals sourced from the input of any GPIO pins
- 232 HP peripheral output signals routed to the output of any GPIO pins
- Signal synchronization for HP peripheral inputs based on HP IO MUX operating clock

**Additional Features:**
- GPIO Filter hardware for input signal filtering
- Glitch Filter hardware for second-time filtering on input signal
- Sigma delta modulated (SDM) output

---

**Footer:** 
Espressif Systems  
Page 44 of ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)