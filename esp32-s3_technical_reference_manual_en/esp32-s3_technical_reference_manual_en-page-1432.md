**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Section Header:**
Register 37.8. RMT_REF_CNT_RST_REG (0x00C8)

**Binary Diagram Description:**
- The diagram shows a binary representation of the register with labels for each bit position.

**Text Descriptions and Definitions in Markdown Format:**

1. **RMT_REF_CNT_RST_CHn (r = 0, 1, 2, 3)**
   - This text describes that this bit is used to reset the clock divider of channel `n`. It also notes its write-back nature.

2. **RMT_REF_CNT_RST_CHm (m = 4, 5, 6, 7)**
   - Similar description as above but for different channels (`m`).

3. **Register 37.9. RMT_CHnSTATUS_REG (n: 0-3) (0x0050+0x4*n)**
   - This text describes a register that records the FSM status of channel `n`.

4. **RMT_MEM_RADDR_EX_CHn**
   - Describes this field as recording the memory address offset when transmitter on channel `n` is using RAM.

5. **RMT_APB_MEM_WADDR_CHn**
   - Describes this field for writing to RAM over APB bus, indicating it records a read-only status (RO).

6. **RMT_STATE_CHn**
   - This text describes that the FSM state of channel `n` can be recorded here.

7. **RMT_MEM_EMPTY_CHn**
   - Indicates when the TX data size is larger than memory size and wrap mode for transmission (`TX`) disabled, this bit will set (RO).

8. **RMT_APB_MEM_WR_ERR_CHn**
   - Describes that if offset address goes out of RAM's available space during writes via APB bus, it sets an error status.

**Footer:**
- "Espressif Systems" and document version information are present at the bottom.
- There is a link to submit documentation feedback.