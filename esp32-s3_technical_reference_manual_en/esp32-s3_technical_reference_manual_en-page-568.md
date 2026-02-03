**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**GoBack Link:** GoBack

**Note Section:**
- For a complete list of all power domains and power domain categories, please check Section **10.4.1**.
- Signals in the above diagram are described below:

**Diagram Description with List Items:**

- `xpdl_rtc_reg`:
  - When `RTC_CNTL_RTC_REGULATOR FORCE_PU` is set to 1, low power voltage regulator is always-on;
  - Otherwise, the low power voltage regulator is off when chip enters Light-sleep and Deep-sleep modes. In this case, the RTC domain is powered by an ultra low-power internal power source.

- `xpdl_dig_reg`:
  - When `RTC_CNTL_DG.Wrap_PD_EN` is enabled, the digital voltage regulator is off when the chip enters Light-sleep and Deep-sleep modes;
  - Otherwise, the digital voltage regulator is always on.

- `xpdl_peri`:
  - When `RTC_CNTL_RTC_PD_EN` is enabled, RTC peripherals are off when chip enters Light-sleep and Deep-sleep modes;
  - Otherwise, the RTC peripherals are always on.
  
- `xpdl_cpu`:
  - When `RTC_CNTL_CPU_PD_EN` is enabled, CPU is off when chip enters Light-sleep and Deep-sleep modes;
  - Otherwise, the CPU is always on.

- `xpdl_pd_peri`:
  - When `RTC_CNTL_DG.PERI_PD_EN` is enabled, the PD Peripherals are off when chip enters Light-sleep and Deep-sleep modes;
  - Otherwise, the PD peripherals are always on.
  
- `xpdl_dg_wrap`: this signal is always the same with `xpdl_dig_reg`.

- `xpdl_wireless`:
  - When `RTC_CNTL_WIFI_PD_EN` is enabled, the wireless circuit is off when chip enters Light-sleep and Deep-sleep modes;
  - Otherwise, the wireless circuit is always on.

- `xpdl_sdio_reg`: see Section **10.3.4.3** below.
  
- `xpdl_ex_crystal`:
  - When `RTC_CNTL_XTL FORCE_PU` is set to 1, the external main crystal clock is always-on;
  - Otherwise, the external main crystal clock is off when chip enters Light-sleep and Deep-sleep modes.

- `xpdl_rc_oscillator`:
  - When `RTC_CNTL_CK8M_FORCE_PU` is set to 1, the fast RC oscillator is always-on.
  - Otherwise, the fast RC oscillator is off when chip enters Light-sleep and Deep-sleep modes.

- RF Circuits and Phase Lock Loop (PLL) are controlled by internal signals and cannot be modified by users.

**Section Title:**
10.3.1 Power Management Unit

**Body Text for Section 10.3.1:**

ESP32-S3’s power management unit controls the power supply to different power domains. The main components of the power management unit include:

- RTC main state machine: generates power gating, clock gating, and reset signals.
- Power controllers: power up and power down different power domains, according to the power gating

**Footer Information:** 
Espressif Systems
Page Number 568
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback