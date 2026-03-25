
```markdown
- TWAIFD_TIMER_OVERFLOW_INT: Triggered when timer overflow occurs.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 38.6 Register Summary.
```

## 38.5 Programming Examples

### 38.5.1 500 Kbit/2 Mbit Example

A common configuration for CAN bus bit rates in the automotive industry is 500 Kbit/s for the nominal bit rate and 2 Mbit/s for the data bit rate. The following example demonstrates how to configure these settings, assuming CAN FD’s clock source is PLL_F8OM and a sample point at 80% of each bit:

```c
uint32 btr;
btr = (4 << 19);        // Time Quanta: 4
btr |= 29;               // Prop: 29
btr |= (10 << 7);        // Phase 1: 10
btr |= (10 << 13);       // Phase 2: 10
btr |= (3 << 27);        // SJW3

REG32_WR(TWAIFD_BTR_REG, btr); // ((29+10+10+1)*4=200*10ns=2us=500Kbit

uint32 btr_fd;
btr_fd = (1 << 19);      // Time Quanta: 1
btr_fd |= 29;            // Prop29
btr_fd |= (10 << 7);     // Phase 1: 10
btr_fd |= (10 << 13);    // Phase 2: 10
btr_fd |= (3 << 27);     // SJW3

REG32_WR(TWAIFD_BTR_FD_REG, btr_fd); // ((29+10+10+1)*1=50*10ns=0.5us=2Mbit
```

#### 38.5.1.1 CAN Frame Transmission

##### 38.5.1.1.1 Sample Code

```c
#define CAN_FD_BASE TWAIFD_DEVICE_ID_VERSION_REG
#define TX_COMMAND_ADDR (CAN_FD_BASE + 0x74)
#define TXT_BUFFER_1_BASE (CAN_FD_BASE + 0x100)

/* Insert CAN frames to TX buffer 1 */
uint32_t frame_format_word = 0;
frame_format_word |= 4;                          // DLC = 4
frame_format_word |= (1 << 7);                   // CAN FD Frame
frame_format_word |= (1 << 9);                   // Switch the bit rate

REG32_WR(TXT_BUFFER_1_BASE, frame_format_word);   // Store the frame format word

uint32_t id_word = (55 << 18);
REG32_WR(TXT_BUFFER_1_BASE + 0x4, id_word);       // Identifier: 55
REG32_WR(TXT_BUFFER_1_BASE + 0x8, 1000);          // Store the identifier word

REG32_WR(TXT_BUFFER_1_BASE + 0xC, 0);             // Transmit at time 1000

REG32_WR(TXT_BUFFER_1_BASE + 0x10, 0xAABBCCDD);   // Data: 0xAA 0xBB 0xCC 0xDD

/* Issue the set ready command */
uint32_t command = 0;
command |= 0x2;                                  // Set ready command
command |= (1 << 8);                            // Choose TX buffer 1
```