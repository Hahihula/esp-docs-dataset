**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Diagram and Figure Caption for Timing Parameters Receiving Data:**
- **Figure:** RMII Timing - Receiving Data

**Table Description with Headings, Min, Typ, Max Values in a Tabular Format under the Diagram:**

| Timing Parameters | Description       | Min  | Typ | Max |
|-------------------|--------------------|------|-----|-----|
| t_CYC            | Clock cycle       | 20   | -   | 20  |
| t_SU             | Setup time         | 4    | -   | ns  |
| t_H              | Hold time          | 1    | -   | ns  |
| t_ID             | Input delay        | 3,5,8| -   | ns  |

**Diagram and Figure Caption for Timing Parameters Transmitting Data:**
- **Figure:** RMII Timing - Transmitting Data

**Table Description with Headings, Min, Typ, Max Values in a Tabular Format under the Diagram:**

| Timing Parameters | Description       | Min  | Typ | Max |
|-------------------|--------------------|------|-----|-----|
| t_CYC            | Clock cycle       | 20   | -   | 20  |
| t_SU             | Setup time         | 4    | -   | ns  |
| t_H              | Hold time          | 1    | -   | ns  |
| t_ODP            | Output delay       | 6,9,12| -  | ns  |

**Section Title:**
24.7 Ethernet DMA Features

**Body Text Description of the Feature and its Functionality:**

The DMA has independent Transmit and Receive engines, and a CSR (Control and Status Registers) space.
- The Transmit engine transfers data from the system memory to the device port (MTL), while the Receive engine transmits data from the device port to the system memory. 
- The controller uses descriptors to efficiently move data from source to destination with minimal Host CPU intervention.

The DMA is designed for packet-oriented data transmission, such as frames in Ethernet.
- The controller can be programmed to interrupt the Host CPU for normal situations, such as the completion of frame transmission or reception, or when errors occur. 

**Footer Information:**
Espressif Systems
474 ESP32 TRM (Version 5.6)
Submit Documentation Feedback