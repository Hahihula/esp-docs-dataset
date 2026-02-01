**Title:**
1. Schematic Design

**Figure Caption and Image Description:**
- Figure 1-5 shows a Reference Circuit Design for a Codec Ground Plane.

**Subtitles with Content:**

1.3. Pin Configuration of ESP32:
   - **1.3.1 Module Power Supply:** 
     At the 3.3 V power supply input pin, it is recommended to add a 100 uF large capacitor with an extra filter capacitor of 0.1 uF close to the module power supply pin.
   
   - **1.3.2 Module Enable:**
     A 10 K pull-up resistor and a 1 uF ground capacitor are highly recommended on CHIP_EN pin to form an RC delay circuit to avoid level instability on CHIP_EN end in power-on process. In addition, CHIP_EN serves as the reset pin, so it is recommended to connect it to a button for the reset operation.
   
   - **1.3.3 Input-only Pins:**
     Some pins of ESP32 can be used for input only, such as CHIP_EN, SENSOR_VP, SENSOR_CAPP, SENSOR_CAPN, SENSORVN, IO34, IO35, etc.

**Note Section (with bullet points):**
- **For example:** 
  - SENSOR_VP, SENSOR_CAPP, SENSOR_CAPN and SENSOR_VN are recommended for use as ADC detection. The recommended voltage detection range is 0 V~2.5 V.
  - Also, adding a 0.1 uF capacitor to the pin close to ESP32 is suggested.

**Additional Information:**
- In ESP32 series modules, SENSOR_CAPP and SENSOR_CAPN pins are not led out; only SENSOR_VP and SENSORVN can be used for input-only purposes.
  
**Footer:**
- Espressif
- Page number 4/19 (bottom left)
- Date January 2019.01