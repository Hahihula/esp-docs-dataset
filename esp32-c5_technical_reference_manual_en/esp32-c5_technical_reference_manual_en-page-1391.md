

```markdown
acceptance filter mode is disabled, filtering is not applied, and each received CAN frame is stored to the RX buffer.

Each filter can be selectively configured to accept only certain types of CAN frame types (CAN 2.0 frame/CAN FD frame) and identifier types (frame with base identifier only, frame with base + extended identifier). Such configuration is available in TWAIFD_FILTER_CONTROL. Each filter is disabled by setting all bits in TWAIFD_FILTER_CONTROL register belonging to this filter to 0. The internal operation of a single acceptance filter instance is illustrated in Figure 38.3-13.

Figure 38.3-13. Frame filters operation (* stands for A/B/C/R based on filter type)

38.3.9.9 Mask Filter

The mask filter checks if the received CAN frame identifier equals to the predefined identifier in TWAIFD_FILTER_X_VAL_REG (X=A, B, C based on filter instance). Only bits given by filter mask in TWAIFD_FILTER_X_MASK_REG are compared.

When using mask filters to filter frames with base identifiers only, set TWAIFD_FILTER_X_MASK_REG[17:0] to 0b00000000000000000000.

38.3.9.10 Range Filter

The range filter determines if the received CAN frame identifier falls within a certain decimal range. The lower threshold of this decimal range is determined by TWAIFD_FILTER_RAN_LOW_REG and the upper threshold is determined by TWAIFD_FILTER_RAN_HIGH_REG.

When using range filters to filter frames with base identifiers only, set TWAIFD_FILTER_RAN_LOW_REG[17:0] to 0b00000000000000000000 and TWAIFD_FILTER_RAN_HIGH_REG[17:0] to 0b11111111111111111111.
```