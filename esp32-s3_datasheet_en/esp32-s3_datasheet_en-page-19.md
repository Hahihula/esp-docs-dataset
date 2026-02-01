**Title: Pins**

---

**Table Title:** Table 2-2 – cont'd from previous page

| Pin       | Glitch^1   | Typical Time Period (µs) |
|-----------|------------|--------------------------|
| GPIO18    | Low-level glitch | 60                       |
|           | High-level glitch | 60                       |
| GPIO19    | Low-level glitch | 60                       |
|           | High-level glitch^2 | 60                       |
| GPIO20    | Pull-down glitch   | 60                       |
|           | High-level glitch^2 | 60                       |

**Footnotes:**
1. Low-level glitch: the pin is at a low level output status during the time period;
2. High-level glitch: the pin is at a high level output status during the time period;
3. Pull-down glitch: the pin is at an internal weak pulled-down status during the time period;
4. Pull-up glitch: the pin is at an internal weak pulled-up status during the time period.

**Additional Information:** Please refer to Table 5-4 DC Characteristics (3.3 V, 25 °C) for detailed parameters about low/high-level and pull-down/up.
GPI019 and GPI020 pins both have two high-level glitches during chip power-up, each lasting for about 60 µs. The total duration for the glitches and the delay are 3.2 ms and 2 ms respectively for GPI019 and GPI020.

---

**Footer:**
Espressif Systems
ESP32-S3 Series Datasheet v2.1

Submit Documentation Feedback