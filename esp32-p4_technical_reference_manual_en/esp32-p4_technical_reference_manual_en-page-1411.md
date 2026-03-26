

```markdown
* VBAT_CHARGER: Indicates whether the battery connected to VDD_BAT needs charging.

These thresholds trigger different interrupts.

• Monitoring modes
There are two monitoring modes based on the way the brown-out detector handles the brown-out signal:

- Mode 0: When Mode 0 is enabled, the brown-out counter starts counting after detecting a brown-out signal. Interrupt and reset signals are generated when the counter reaches the thresholds defined by LP_ANA_BOD_MODEO_RESET_WAIT and LP_ANA_BOD_MODEO_INTR_WAIT, respectively. This helps filter out noise on the monitored pins. Configure LP_ANA_BOD_MODEO_RESET_SEL to select the reset options:

  * 0: Reset the chip.
  * 1: Reset the system.

- Mode 1: Mode 1 is the default mode, which resets the system immediately upon detecting under-voltage.

• Voltage-monitoring thresholds
The voltage-monitoring threshold is configured in the analog circuit by the analog I2C master. The threshold configuration registers are as follows. BIAS is the slave of the analog I2C master. The address of BIAS is 0x6a. REGXX indicates the register address of BIAS, and [x:x] indicates the bits of this register.

- BIAS_OR_DREFL_VBAT (REG08[7:5]): threshold for releasing the under-voltage state of VDD_BAT
- BIAS_OR_DREFH_VBAT (REG08[4:2]): under-voltage threshold of VDD_BAT
- BIAS_OR_DREFL_VDDA (REG09[7:5]): threshold for releasing the under-voltage state of VDD_ANA
- BIAS_OR_DREFH_VDDA (REG09[4:2]): under-voltage threshold of VDD_ANA
- BIAS_OR_DREFL_VBAT_CHARGER (REG10[7:5]): threshold for releasing the under-voltage state of battery connected to VDD_BAT
- BIAS_OR_DREFH_VBAT_CHARGER (REG10[4:2]): under-voltage threshold of battery connected to VDD_BAT

The relationship between the threshold configuration of VBAT/VDDA and voltage is:

- 0: 2.0 V
- 1: 2.1 V
- 2: 2.2 V
- 3: 2.3 V
- 4: 2.4 V
- 5: 2.5 V
- 6: 2.6 V
- 7: 2.7 V

The relationship between the threshold configuration of VBAT_CHARGER and voltage is:

- 0: 2.2 V
```