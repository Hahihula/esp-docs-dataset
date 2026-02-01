**Title:**
2. PCB Layout Design

**Subtitle:**
2.2.3. Positioning Chip Components

**Body Text:**
It is recommended to place the chip components and their peripherals together, especially the filter capacitor for the power supply. These capacitors must be placed as close to the power pins as possible and distributed evenly. Please make sure you have a filter capacitor near each power pin, but do not stack all the capacitors in one place.

For the sake of routing and ground splitting, modules sharing the same ground plane should be placed near, as well as the functionally related modules (Codec, PA power amplifier and speaker of Audio chip, as well as USB interface, charging module and battery interface). See the picture below.

**Image Caption:**
Figure 2-8. Reference Placement for Chip Components

**Footer Information:**
Espressif
13/19
2019.01