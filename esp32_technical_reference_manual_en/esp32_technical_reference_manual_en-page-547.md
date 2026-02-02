**Title: Chapter 25 Two-Wire Automotive Interface (TWAI)**

---

### Figure Caption:
- **Figure 25.5-4. Error State Transition**

---

#### Text Content:

1. Set REC to O
2. Set TEC to 127
3. Set the TWAI_BUS_OFF_ST bit to 1
4. Enter Reset Mode

The Error Warning Interrupt is triggered whenever the value of the **TWAI_BUS_OFF_ST** bit (or the **TWAI_ERR_ST** bit) changes.

To return to the Error Active state, the TWAI controller must undergo Bus-Off recovery. Bus-Off recovery requires the TWAI controller to observe 128 occurrences of 11 consecutive Recessive bits on the bus. To initiate Bus-Off recovery (after entering the Bus-Off state), the TWAI controller should enter Operation Mode by setting the **TWAI_RESET_MODE** bit to O. The TEC tracks the progress of Bus-Off recovery by decrementing the TEC each time the TWAI controller observes 11 consecutive Recessive bits. When Bus-Off recovery has completed (i.e., TEC has decremented from 127 to O), the **TWAI_BUS_OFF_ST** bit will automatically be reset to O, thus triggering the Error Warning Interrupt.

---

#### Subtitle:
- **25.5.8 Error Code Capture**

The Error Code Capture (ECC) feature allows the TWAI controller to record the error type and bit position of a TWAI bus error in the form of an error code. Upon detecting a TWAI bus error, the Bus Error Interrupt is triggered and the error code is recorded in the **TWAI_ERR_CODE_CAP_REG**. Subsequent bus errors will trigger the Bus Error Interrupt, but their error codes will not be recorded until the current error code is read from the **TWAI_ERR_CODE_CAP_REG**.

The following Table 25.5-11 shows the fields of the TWAI_ERR_CODE_CAP_REG:

| Bit | Bit Information |
|-----|------------------|
| 31-8 | Reserved         |
|     | ERRC.1^          |
|      |                 |
|    7 | Bit              |
|     | DIR2             |
|     | SEG.4^           |
|     | SEG.3^           |
|     | SEG.0^           |

**Notes:**
- **ERRC:** The Error Code (ERC) indicates the type of bus error; OO for bit error, O1 for form error, 10 for stuff error, and other types.
  
---

#### Footer:
- Espresso Systems
- ESP32 TRM (Version 5.6)
- Submit Documentation Feedback

--- 

### Table Content:

| Bit | Bit Information |
|-----|------------------|
| 31-8 | Reserved         |
|     | ERRC.1^          |
|      |                 |
|    7 | Bit              |
|     | DIR2             |
|     | SEG.4^           |
|     | SEG.3^           |
|     | SEG.0^           |

**Notes:**
- **ERRC:** The Error Code (ERC) indicates the type of bus error; OO for bit error, O1 for form error, 10 for stuff error, and other types.

--- 

### Diagram Description:
The diagram in Figure 25.5-4 illustrates different states related to TWAI's error handling mechanism:

- **TEC, REC**: Shows the transition from Error Active state (default) through various stages including Error Warning Interrupts.
- The chart includes a timeline with specific values for TEC and REC indicating transitions between Bus Off status.

### Notes:
1. Note 3: This is indicated in relation to TWAI BUS >255, but no further details are provided within the visible text section of this page capture image.