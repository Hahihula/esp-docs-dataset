**Title:**
2. PCB Layout Design

**Body Text:**
- It is recommended to separate different power traces from each other by ground traces and to plate copper for power supplies on adjacent layers to avoid overlapping. It helps to reduce mutual interference.

In the figure below, red and purple represent power copper for different purposes, and blue represents ground copper.

**Figure Caption (Image):**
Figure 2-10: Recommended Power Routing

**Subtitle:**
2.3.2. Ground Traces Routing

**Body Text:**
Different reference ground planes should be separated. Please keep the cutting lines consistent on all layers and drill more ground holes around the OR resistors that connect to the reference grounds. It is also recommended to drill as many ground holes as possible close to the devices’ GND pins, especially in the area of the power supply’s filter capacitor.

If there is a thermal pad in the middle of the chip, it is suggested to drill no less than 9 evenly-distributed ground holes.

**Footer:**
Espressif
15/19
2019.01