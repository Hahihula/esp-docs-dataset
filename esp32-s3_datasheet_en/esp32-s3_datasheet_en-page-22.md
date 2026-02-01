**Title: Pins**

---

**Subtitle: Cont'd from previous page**

**Table Headers:**  
Pin No., GPIO, FO Type^3, F1, F2, F3, F4, Type

**Table Content (Partial):**
- Pin 35: GPIO32, SPID I/O/T, GPIO32
- Pin 36: GPIO48, SPICLK_N_DIFF O/T, GPIO48
- Pin 37: GPIO47, SPICLK_P_DIFF O/T, GPIO47
- Pin 38: GPIO33, FSPIHD I/O/T, GPIO33
- Pin 39: GPIO34, FSPICSO I/O/T, GPIO34
- Pin 40: GPIO35, FSPIID I/O/T, GPIO35

**Continued Table Content (Partial):**
- Pin 41: GPIO36, SPICLK I/O/T, GPIO36
- Pin 42: GPIO37, FSPIQ I/O/T, GPIO37
- Pin 43: GPIO38, SPIWP O/T, GPIO38
- Pin 44: GPIO39, CLK_OUT3 O/T, GPIO39
- Pin 45: GPIO40, CLK_OUT2 O/T, GPIO40

**Continued Table Content (Partial):**
- Pin 47: GPIO41, CLK_OUT1 I/O/T, GPIO41
- Pin 48: GPIO42, MTMS I/O/T, GPIO42
- Pin 49: GPIO43, UOTXD O, GPIO43
- Pin 50: GPIO44, UORXD I/O/T, GPIO44

**Continued Table Content (Partial):**
- Pin 51: GPIO45, I/O/T, GPIO45
- Pin 52: GPIO46, I/O/T, GPIO46

---

**Footnotes:**  
1. Bold marks the default pin functions in the default boot mode.
2. For more information about the boot mode, see Section **3.1 Chip Boot Mode Control**.

**Regarding highlighted cells,** refer to [Section 2.3.4 Restrictions for GPIOs and RTC_GPIOs](#).

---

**Each IO MUX function (Fn_n = 0 ~ 4) is associated with a type:**
- I – input.
- O – output.
- T – high impedance.

**IO MUX functions description:**  
- Fn_n = 1, the pin's signal of Fn is always 1.  
- Fn_n = 0, if the pin assigned function other than Fn, the input signal of Fn is always θ.

---

**Footer:**
Espressif Systems  
ESP32-S3 Series Datasheet v2.1

[Submit Documentation Feedback](#)