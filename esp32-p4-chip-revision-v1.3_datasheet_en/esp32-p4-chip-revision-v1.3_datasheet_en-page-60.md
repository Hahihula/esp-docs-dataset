**4 Functional Description**

- **MV merge for outputting**: The MV of each macroblock to memory.

- **Region of interest (ROI)**: It can configure up to eight rectangular ROI areas at any position. These ROI areas have fixed priorities and can overlap with each other. Each ROI area can be assigned a fixed QP or QP offset, and a non-ROI area can be specified with a QP offset.

**Pin Assignment**

The H264 encoder does not directly interact with IOs, so it has no pins assigned.

---

**4.2.1.6 MIPI CSI**

ESP32-P4 includes one MIPI CSI interface for connecting cameras of the MIPI interface.

- **Feature List**
  - Compliant with MIPI CSI-2
  - Compliant with DPHY v1.1
  - 2-lane x 1.5 Gbps

- **Input formats**: RGB888, RGB666, RGB565, YUV422, YUV420, RAW8, RAW10, and RAW12

**Pin Assignment**

The MIPI CSI interface uses the dedicated digital pins 42–48.

---

**4.2.1.7 MIPI DSI**

ESP32-P4 features a MIPI DSI interface for connecting displays of the MIPI interface.

- **Feature List**
  - Compliant with MIPI DSI
  - Compliant with DPHY v1.1

- **2-lane x 1.5 Gbps**

- **Input formats**: RGB888, RGB666, RGB565, and YUV422

- **Output formats**: RGB888, RGB666, and RGB565

- Using the video mode to output video stream
- Outputting image patterns

**Pin Assignment**

The MIPI DSI interface uses the dedicated digital pins 34–40.

---

**4.2.2 Connectivity Interface**

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

Espressif Systems

ESP32-P4 Series Datasheet v0.6
[Submit Documentation Feedback](#)