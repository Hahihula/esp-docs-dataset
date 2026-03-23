

# Chapter 36
## Motor Control PWM (MCPWM)

### 36.1 Overview

The **Motor Control Pulse Width Modulator** (MCPWM) peripheral is intended for motor and power control. It provides six PWM outputs that can be set up to operate in several topologies. One common topology uses a pair of PWM outputs driving an H-bridge to control motor rotation speed and rotation direction.

The MCPWM can be divided into five main modules: PWM timers, PWM operators, Capture module, Event Task Matrix (ETM) module, and Fault Detection module. Each PWM timer provides timing references that can either run freely or be synced to other timers or external sources. Each PWM operator has all necessary control resources to generate waveform pairs for one PWM channel. The Capture module is used for systems that need to accurately time external events. The ETM module responds to tasks received by the MCPWM, generating corresponding events depending on the state of motion. The Fault Detection module is used to capture external faults, allowing the system to respond by choice.

ESP32-C6 has one MCPWM peripheral, which is **MCPWM0**.

### 36.2 Features

An MCPWM peripheral has one clock divider (prescaler), three PWM timers, three PWM operators, a Capture module, an ETM module, and a Fault Detection module. MCPWM’s core clock can be selected from three clock sources: `PLL_F160M_CLK`, `XTAL_CLK`, and `RC_FAST_CLK` (configured by `PWM_CLKM_SEL` field in PCR register). Figure 36.2-1 shows the submodules inside MCPWM and the signals on the interface. PWM timers are used for generating timing references. The PWM operators generate the desired waveform based on the timing references. Any PWM operator can be configured to use the timing references of any PWM timers.

Different PWM operators can use the same PWM timer’s timing reference to generate PWM signals, or different PWM timers’ values to generate separate PWM signals. Different PWM timers can also be synchronized together.

Below is an overview of the submodules’ functionality in Figure 36.2-1:

*   **PWM Timers 0, 1, and 2:**
    *   Every PWM timer has a dedicated 8-bit clock prescaler.
    *   The 16-bit counter in the PWM timer can work in count-up mode, count-down mode, or count-up-down mode.
    *   A hardware sync or software sync can trigger a reload on the PWM timer with a phase register. It will also trigger the prescaler’s restart, so that the timer’s clock can also be synced. The source of the hard sync can come from any GPIO or any other PWM timer’s `sync_out`. The source of the soft sync comes from writing toggle value to the **MCPWM_TIMERx_SYNC_SW** bit.