**Title:**
2 Pins

**Figure Caption (Top):**
Figure 2-3. ESP32-C3 Power Scheme

**Body Text and Diagrams with Descriptions:**

1. **Diagram Description:** 
   - The diagram shows the power scheme for an ESP32-C3 chip, indicating connections between VDD3P3_RTC, VDD3P3_CPU, VDDA1_VDDA2 pins to Low Power Voltage Regulator (Analog), Digital System Voltage Regulator, and R_SPI. It also includes connections labeled as RTC IO, RTC, Digital System, and Digital IO.

2. **Subsection Title:**
   2.5.3 Chip Power-up and Reset

3. **Body Text under Subsection:**
   - "Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_EN – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_EN as well as power-up and reset timing, see Figure 2-4 and Table 2-11."

**Figure Caption (Bottom):**
Figure 2-4. Visualization of Timing Parameters for Power-up and Reset

**Graph Description:**
The graph shows various voltage levels over time with labels such as t_STBL, VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_CPU, CHIP_EN, t_RST, and RST. The x-axis represents the timeline (t), while different sections of the curve indicate specific timing parameters for power-up and reset.

**Footer:**
- "Espressif Systems"
- Page number 27
- Document title: ESP32-C3 Series Datasheet v2.2

**Link Text at Bottom Right Corner:** 
"Submit Documentation Feedback"

(Note: The text in the image is transcribed as accurately described from visual content.)