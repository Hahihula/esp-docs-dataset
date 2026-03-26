

```markdown
Register 52.23. PMT_RWUFFR_REG (0x0028)

WKUPPKTFILTER When RWKPTR is 0 ~ 3, configures the masking of filter 0 ~ 3 wakeup frame.
Bit[30:0] corresponds to offset+j (j = 0 ~ 30).
Bit[31] has to be 0. 0: Unmask
    1: Mask

When RWKPTR is 4, bit[3]/bit[11]/bit[19]/bit[27] configure the target address type, and
bit[0]/bit[8]/bit[16]/bit[24] configure whether to enable filter 0 ~ 3.
    0: Unicast/Disable
    1: Multicast/Enable

When RWKPTR is 5, configures the offset of the filter 0 ~ 3 masked byte.
Bit[7:0] configures the offset of filter 0 masked byte, and [31:24] configures the offset of filter 3
masked byte.

When RWKPTR is 6 ~ 7 configures the 16-bit CRC value of filter 0 ~ 3 masked byte starting from
offset based on the formula:
G(x) = x^16 + x^15 + x^2 + 1

Bit[7:0] configures the CRC value of filter 0 or filter 2 masked byte when RWKPTR is 6 or 7 respectively, and bit[31:16] configures the CRC value of filter 1 or filter 3 masked byte when RWKPTR is
6 or 7 respectively.
(R/W)
```