

```markdown
Chapter 53 Two-Wire Automotive Interface (TWAI)

Figure 53.4-1. Acceptance Filter

The TWAI controller Acceptance Filter allows the 32-bit Acceptance Code and Mask Values to either define a single filter (i.e., Single-filter mode), or two filters (i.e., Dual-filter mode). How the Acceptance Filter interprets the 32-bit code and mask values is dependent on the filter mode and the format of received messages (i.e., SFF or EFF).

53.4.5.1 Single-Filter Mode

Single Filter mode is enabled by setting the TWAI_ACCEPTANCE_FILTER_MODE bit to 1. This will cause the 32-bit code and mask values to define a single filter. The single filter can filter the following bits of data or remote frames:

*   SFF
    -   The entire 11-bit ID
    -   RTR bit
    -   Data byte 1 and Data byte 2
*   EFF
    -   The entire 29-bit ID
    -   RTR bit

The following Figure 53.4-2 illustrates how the 32-bit code and mask values will be interpreted under Single-filter mode.

53.4.5.2 Dual-Filter Mode

Dual-filter mode is enabled by clearing the TWAI_ACCEPTANCE_FILTER_MODE bit to 0. This will cause the 32-bit code and mask values to define a two separate filters referred to as filter 1 or filter 2. Under Dual-filter mode, a message will be accepted if it is accepted by one of the two filters.

The two filters can filter the following bits of data or remote frames:

*   SFF
    -   The entire 11-bit ID
    -   RTR bit
    -   Data byte 1 (for filter 1 only)
```