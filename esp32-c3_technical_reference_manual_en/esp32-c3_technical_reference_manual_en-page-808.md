

```markdown
## 31.4.6.1 Single Filter Mode

Single Filter Mode is enabled by setting the `TWAI_RX_FILTER_MODE` bit to 1. This will cause the 32-bit code and mask values to define a single filter. The single filter can filter the following bits of a data or remote frame:

*   SFF
    *   The entire 11-bit ID
    *   RTR bit
    *   Data byte 1 and Data byte 2

*   EFF
    *   The entire 29-bit ID
    *   RTR bit

The following Figure 31.4-2 illustrates how the 32-bit code and mask values will be interpreted under Single Filter Mode.

![Figure 31.4-2. Single Filter Mode](image)

## 31.4.6.2 Dual Filter Mode

Dual Filter Mode is enabled by clearing the `TWAI_RX_FILTER_MODE` bit to 0. This will cause the 32-bit code and mask values to define a two separate filters referred to as filter 1 or filter 2. Under Dual Filter Mode, a message will be accepted if it is accepted by one of the two filters.

The two filters can filter the following bits of a data or remote frame:

*   SFF
    *   The entire 11-bit ID
    *   RTR bit
    *   Data byte 1 (for filter 1 only)

*   EFF
```