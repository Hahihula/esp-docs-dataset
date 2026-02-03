**Chapter Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Section Heading and Content:**

- **CMD_RSV is reserved in the current implementation. The ESP32-S3 will ignore this command when it receives it.**
  
- **CMD_REP repeats the last (non-CMD_REP) command a certain number of times. It’s intended goal is to compress command streams which repeat the same CMD_CLK instruction on multiple times. A command like CMD_CLK can be followed by multiple CMD_REP commands. The number of repetitions done by one CMD_REP can be expressed as \(no\_repetitions = (R1 \times 2 + R0) \times (4^{cmd\_rep\_count})\), where cmd_rep_count is how many CMD_REP instructions went directly before it. Note that the CMD_REP is only intended to repeat a CMD_CLK command. Specifically, using it on a CMD_FLUSH command may lead to an unresponsive USB device, needing an USB reset to recover.**

**Subsection Title:**
33.3.6 USB-to-JTAG Interface: CMD_REP Usage Example

**Body Text and List of Commands with Explanation (Example):**

Here is a list of commands as an illustration of the use of CMD_REP. Note each command is a nibble; in this example the bitwise command stream would be 0x0D 0x5E 0xCF.

1. **0x0 (CMD_CLK: cap=0, tdi=0, tms=0)**
2. **0xD (CMD_REP: R1=0, R0=1)**
3. **0x5 (CMD_CLK: cap=1, tdi=0, tms=1)**
4. **0xE (CMD_REP: R1=1, R0=0)**
5. **0xC (CMD_REP: R1=0, R0=0)**
6. **0xF (CMD_REP: R1=1, R0=1)**

This is what happens at every step:

- TCK is clocked with the TDI and TMS lines set to 0.
- No data is captured.

**List Explanation of Steps for CMD_REP Example**

1. **TCK is clocked (TDI = 0, tdi=0, tms=0)**
2. **TCK is clocked another \( (0 \times 2 + 1) \times (4^0) = 1\) time with the same settings as step 1.**
3. **TCK is clocked again (\(1 \times 2 + 0\) \times (4^0) = 2\) times with the same settings as step 3.**
4. Nothing happens: \( (0 \times 2 + 0) \times (4^1) = 0\). Note that this does increase cmd_rep_count for the next step.
5. **TCK is clocked another (\(1 \times 2 + 1\) \times (4^2) = 48\) times with the same settings as step 3.**

In other words: This example stream has the same net effect as command 1 twice, then repeating command 3 for 51 times.

**Subsection Title and Content:**
33.3.7 USB-to-JTAG Interface: Response Capture Unit

**Body Text Explanation of Response Capture Unit Functionality:**

The response capture unit reads the TDO line of the internal JTAG bus and captures its value when the command parser executes a CMD_CLK with cap=1. It puts this bit into an internal shift register, and writes a byte into the USB buffer when 8 bits have been collected. Of these 8 bits, the least significant one is the one that is read from TDO the earliest.

As soon as either 64 bytes (512 bits) have been collected or a CMD_FLUSH command is executed, the response capture unit will make the buffer available for the host to receive. Note that the interface to the USB logic is double-buffered. This way, as long as USB throughput is sufficient, the response capture unit can always receive more data: while one of the buffers is waiting to be sent to the host, the other one can receive.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback