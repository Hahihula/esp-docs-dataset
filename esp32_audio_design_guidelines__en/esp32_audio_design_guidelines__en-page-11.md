**Title: PCB Layout Design**

During Audio PCB Layout design, pay attention to the following sections:
- General principles of PCB Layout
- Key points of PCB Layout design
- Power traces, ground traces, and signal traces

### 2.1. General Principles of PCB Layout

#### 2.1.1. PCB Layers

A four-layer PCB design is recommended.

- **First layer:** TOP layer for ESP32 module and most other chips.
- Second layer: GND layer with a complete GND plane
- Third layer: POWER layer to route power traces and part of signal traces
- Fourth layer: BOTTOM layer, on which some components are placed, and also power traces and signal traces are routed.

**Note:**  
Components can be placed either on the TOP layer or BOTTOM layer according to the actual situation,
but it is recommended to set the adjacent layer of ESP32 module as GND layer. Even if ESP32 module
is placed on the BOTTOM layer, it is recommended to set the third layer as a GND layer and the second 
layer as a POWER layer.

#### 2.1.2. General Guidelines for Routing Traces

General guidelines for routing traces are as follows:
- Try to plan out the shortest route and pass through the least holes, avoid unnecessary bending and holes.
- Use obtuse angles to keep the layout as clean and tidy as possible, avoid using right
angles and acute angles or hiding small line segments among these angles
- Avoid routing traces on the layers under crystal oscillator, large inductance devices 
and other sensitive devices.

For example:

---

**Footer:**
Espressif  
8/19  
2019.01