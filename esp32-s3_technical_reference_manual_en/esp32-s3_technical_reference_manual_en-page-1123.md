```markdown
### Figure Title:
Figure 30.5-5: GP-SPI State Machine in Master Mode

### Flowchart Description:

1. **IDLE**
   - Condition: `SPI_USR=0`
   
2. **CONF**
   - Conditions checked based on `SPI_USR_CONF=0` and other conditions.
   - If condition is not satisfied, it loops back to IDLE.

3. **PREP**
   - Conditions related to `SPI_CS_SETUP=1`, `SPI_USR_COMMAND=1`, etc., are evaluated here if they're met; otherwise loop continues or transitions based on specific checks like `CMD` and `ADDR`.

4. **CMD**
   - Condition: `CMD Condition is not satisfied`
   
5. **ADDR**
   - Condition: `ADDR Condition is not satisfied`

6. **DUMMY**
   - Conditions related to `SPI_CS_DUMMY=0`, etc., are evaluated here if they're met; otherwise loop continues or transitions based on specific checks like `DOUT` and others.

7. **DIN**
   - Condition checked for `DIN Condition is not satisfied`

8. **DOUT**
   - Condition: `DOUT Condition is not satisfied`
   
9. **DONE**
   - Conditions related to various states are evaluated here if they're met; otherwise loop continues or transitions based on specific checks like `SPI_CS_HOLD=1` and others.

### Additional Information:
- The flowchart illustrates the state machine behavior of a GP-SPI controller in master mode.
- Each box represents different conditions that need to be satisfied for transitioning between states. 
- Arrows indicate possible paths depending upon whether certain conditions are met or not, leading back into previous stages if necessary (e.g., "is not satisfied" loops).

### Footer:
- ESP32-S3 TRM (Version 1.7)
```