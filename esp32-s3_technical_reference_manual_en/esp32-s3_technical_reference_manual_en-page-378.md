**Title: Chapter 3 GDMA Controller (GDMA)**

**Subtitle: Register 3.4. GDMA_IN_LINK_CHn_REG**

**Body Text:**
- **Register Description:** 
  - `GDMA_INLINK_ADDR_CHn`: This register stores the 20 least significant bits of the first receive descriptor's address.
  - `GDMA_INLINK_AUTO_RET_CHn`: Set this bit to return to current receive descriptor’s address, when there are some errors in current receiving data. (R/W)
  - `GDMA_INLINK_STOP_CHn`: Set this bit to stop GDMA’s receive channel from receiving data. (R/W/SC)
  - `GDMA_INLINK_START_CHn`: Set this bit to enable GDMA's receive channel for data transfer.
  - `GDMA_INLINK_RESTART_CHn`: Set this bit to mount a new receive descriptor. (R/W/SC)
  - `GDMA_INLINK PARK CHn`: 
    - "1: the receive descriptor’s FSM is in idle state; O: the receive descriptor’s FSM is working." (RO)

**Footer:**  
- Page number and document version information:
  - "378 ESP32-S3 TRM (Version 1.7)"
- Company name at bottom left corner.
- Link for submitting documentation feedback.

**Diagram Description in Text Format:**
- A diagram showing the layout of register `GDMA_IN_LINK_CHn_REG` with various bits labeled, such as `GDMA_INLINK_ADDR_CHO`, `GDMA_INLINK_RESET_CHO`, etc. The labels indicate different sections and their corresponding bit positions (e.g., 31 to 0). There is also a note indicating that the diagram shows "register layout" for GDMA IN LINK CHn REG.

**Navigation Link:**
- A link labeled "GoBack".