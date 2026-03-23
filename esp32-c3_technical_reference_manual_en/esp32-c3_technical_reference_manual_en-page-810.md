

```markdown
TEC, REC   0       Error Warning Limit (default 96)      127        TEC Limit > 255         Note 3
            |-----------------------------------------------|-----------------------------|
Error Active     Error Passive                           Bus Off                     |
                 |<-------- Error Warning Interrupt -------->|<--------- Error Warning Interrupt --------->
                 |<-------- Error Passive Interrupt -------->|

Error status   0       1        1
Bus status

TEC : Tx Error Counter
REC : Rx Error Counter

Figure 31.4-4. Error State Transition


31.4.7.1    Error Warning Limit

The Error Warning Limit (EWL) is a configurable threshold value for the TEC and REC, which will trigger an interrupt when exceeded. The EWL is intended to serve as a warning about severe TWAI bus errors, and is triggered before the TWAI controller enters the Error Passive state. The EWL is configured in `TWAI_ERR_WARNING_LIMIT_REG` and can only be configured whilst the TWAI controller is in Reset Mode. The `TWAI_ERR_WARNING_LIMIT_REG` has a default value of 96. When the values of TEC and/or REC are larger than or equal to the EWL value, the `TWAI_ERR_ST` bit is immediately set to 1. Likewise, when the values of both the TEC and REC are smaller than the EWL value, the `TWAI_ERR_ST` bit is immediately reset to 0. The Error Warning Interrupt is triggered whenever the value of the `TWAI_ERR_ST` bit (or the `TWAI_BUS_OFF_ST`) changes.

31.4.7.2    Error Passive

The TWAI controller is in the Error Passive state when the TEC or REC value exceeds 127. Likewise, when both the TEC and REC are less than or equal to 127, the TWAI controller enters the Error Active state. The Error Passive Interrupt is triggered whenever the TWAI controller transitions from the Error Active state to the Error Passive state or vice versa.

31.4.7.3    Bus-Off and Bus-Off Recovery

The TWAI controller enters the Bus-Off state when the TEC value exceeds 255. On entering the Bus-Off state, the TWAI controller will automatically do the following:

*   Set REC to 0
*   Set TEC to 127
*   Set the `TWAI_BUS_OFF_ST` bit to 1
*   Enter Reset Mode

The Error Warning Interrupt is triggered whenever the value of the `TWAI_BUS_OFF_ST` bit (or the `TWAI_ERR_ST` bit) changes.

To return to the Error Active state, the TWAI controller must undergo Bus-Off Recovery. Bus-Off Recovery requires the TWAI controller to observe 128 occurrences of 11 consecutive recessive bits on the bus. To initiate Bus-Off Recovery (after entering the Bus-Off state), the TWAI controller should enter Operation Mode
```