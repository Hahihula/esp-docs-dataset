**4 Functional Description**

---

### Pin Assignment

For the CAM interface of the image signal processor, the pins used can be chosen from any GPIOs via the GPIO Matrix.

#### 4.2.1.3 Pixel-Processing Accelerator (PPA)

ESP32-P4 includes a pixel-processing accelerator (PPA) with scaling-rotation-mirror (SRM) and image blending (BLEND) functionalities.

**Feature List**
- Image rotation, scaling, and mirroring by SRM:
  - Input formats: ARGB8888, RGB888, RBG565, YUV420
  - Output formats: ARGB8888, RBG888, RBG565, YUV420
- Counterclockwise rotation angles: 0°, 90°, 180°, 270°
- Horizontal and vertical scaling with scaling factors of 4-bit integer part and 8-bit fractional part.
- Horizontal and vertical mirroring

**Feature List**
- Blending two layers of the same size and filling images with specific pixels by BLEND:
  - Input formats: ARGB8888, RBG888, RGB565, L4, L8, A4, A8
  - Output formats: ARGB8888, RBG888, RBG565

- Layer blending based on the Alpha channel. If layers lack an Alpha channel, it can be provided through register configuration.
- Special color filtering by setting color-key ranges of foreground and background layers.

---

### 4.2.1.4 LCD and Camera Controller (LCD_CAM)

The pixel-processing accelerator does not directly interact with IOs, so it has no pins assigned.

**Pin Assignment**

#### The LCD and Camera controller (LCD_CAM) on the ESP32-P4

- Consisting of an independent LCD control module and a camera control module.
- Is versatile component designed to facilitate interfacing with both LCDs and cameras.

**Feature List**
- Operation modes:
  - LCD master TX mode
  - Camera slave RX mode
  - Camera master RX mode
  
- Simultaneous connection to an external LCD and a camera

---

Espressif Systems  
58  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)