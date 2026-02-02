**Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Subtitle:**
9.3.8 Power-Gating Implementation

**Figure Description and Caption:**
- **Figure:** Figure 9.3-8. RTC States.
- The figure shows a flowchart with states such as DIG Active, ULP-coprocessor done, touch done, RTC Active, RTC Sleep.

**Body Text:**
The switch among power-gating states can be seen in Figure 9.3-8. The actual power-control signals could also be set by software as force-power-up (FPU) or force-power-down (FPD). Since the power domains can be power-gated independently, there are many combinations for different applications. Table 9.3-1 shows how the power domains in ESP32 are controlled.

**Table Description and Caption:**
- **Table:** Table 9.3-1. RTC Power Domains
- The table lists various components (RTC Digital Core, RTC Peripherals, etc.) with their corresponding states for DIG Active, RTC Active, RTC Sleep options under S/W Options FPU/FPD.

**Notes on the Table:**
1. The power-domain RTC core is always-on and the FPU/FPD option not available.
2. Power-domain RTC peripherals include most of fast logic in RTC (ULP co-processor, sensor controllers).
3. When ULP co-processor works as retention memory or when it uses RTC slow memory for working purposes.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 
188