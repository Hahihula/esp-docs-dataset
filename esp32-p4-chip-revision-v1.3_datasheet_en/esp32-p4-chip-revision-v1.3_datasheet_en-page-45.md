**Title: Functional Description**

---

**4 Functional Description**

- **GPIO simple input and output**
- HP GPIO Wakeup

HP IO MUX has the following features:

- Control of 55 GPIOs (GPIO0-GPIO54) for HP peripherals.
- A configuration register provided for each GPIO pin, to control the pin's input/output, pull-up/pull-down, drive strength, and function selection.

Better high-frequency digital performance achieved by routing some digital signals (SPI, EMAC) directly from HP IO MUX to peripherals.

LP GPIO matrix has the following features:

- A full-switching matrix between the LP peripheral input/output signals and the LP GPIO pins
- 14 LP peripheral input signals sourced from the input of any LP GPIO pins
- 14 LP peripheral output signals routed to the output of any LP GPIO pins

GPIO Filter hardware for input signal filtering

GPIO simple input and output

LP GPIO Wakeup

LP IO MUX has the following feature:

- Control of 16 LP GPIO pins (GPIO0-GPIO15) for LP peripherals.
- A configuration register provided for each LP GPIO pin, to control the pin's input/output, pull-up/pull-down, drive strength, function selection, and IO MUX selection.

---

**4.1.4.2 Reset**

ESP32-P4 provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. All reset types mentioned above (except Chip Reset) preserve the data stored in internal memory.

- **Four reset types:**
  - **CPU Reset:** resets CPU core. HP CPU0, HP CPU1, and LP CPU can be reset independently:
    - *HP CPU0 will be automatically released from reset after chip power-up.*
    - *HP CPU1 is at reset by default after chip power-up, and needs to be manually released from reset.
  - **LP CPU:** is at reset after chip power-up, and needs to be manually released from reset by configuring the power management unit (PMU).
  - **Core Reset:** resets the whole digital system except for LP AON. HP core and LP core can be reset independently: HP Core Reset resets HP CPU0, HP CPI1, HP peripherals, HP GPIO, etc., and LP Core Reset resets LP CPU and LP peripherals.
  - **System Reset:** resets the whole digital system, including the LP system.
  - **Chip Reset:** resets the whole chip.

---

**Footer**

Espressif Systems  
45 ESP32-P4 Series Datasheet v0.6

[Submit Documentation Feedback](#)