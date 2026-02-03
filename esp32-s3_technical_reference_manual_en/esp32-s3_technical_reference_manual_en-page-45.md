**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
Table 1.4-1 – cont’d from previous page

| Name       | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| imm2       | 7-bit unsigned immediate value ranging from 0 to 254 with an interval of 2. This is used to show the size of the updated read/write operation address value. |
| imm4       | 8-bit signed immediate value ranging from -256 to 252 with an interval of 8. This is used to show the size of the updated read写operation address value. |
| imm16      | 8-bit signed immediate value ranging from -2048 to 2032 with an interval of 16. This is used to show the size of the updated read/write operation address value. |
| imm16f     | 4-bit signed immediate value ranging from -128 to 112 with an interval of 16. This is used to show the size of the updated read写operation address value. |

**Body Text:**
Some instructions have multiple operands with the same function. Those operands are distinguished by adding numbers after field names. For example, the EE.LDF.128.IP instruction has four fu registers, fu0 ~ 3. They are used to store 128-bit data read from memory.

**Subsection Title:**
1.5 Components of Extended Instruction Set

**Sub-subsection Title and Content:**
1.5.1 Registers
This section introduces all kinds of registers related to ESP32-S3’s extended instruction set, including the original registers defined by Xtensa as well as customized registers. For register information, please refer to Table 1.5-1.

**Table Header for Subsection (Table 1.5-1):**
Table 1.5-1: Register List of ESP32-S3 Extended Instruction Set

| Register Mnemonics | Quantity | Bit Width | Access   | Type                |
|--------------------|----------|-----------|----------|---------------------|
| AR                 | 16       | 32        | R/W      | General-purpose registers |
| FR                  | 16       | 32        | R/W      | General-purpose registers to FPU |
| QR                  | 8        | 128       | R/W      | Customized general-purpose registers |
| SAR                 | 1        | 6         | R/W      | Special register    |
| SAR_BYTE           | 1        | 4         | R/W      | Customized special register |
| ACCX                | 1        | 40        | R/W      | Customized special register |
| QACC_H              | 1        | 160       | R/W      | Customized special register |
| QACC_L              | 1        | 160       | R/W      | Customized special register |
| FFT_BIT_WIDTH      | 1        | 4         | R/W      | Customized special register |
| UA_STATE           | 1        | 128       | R/W      | Customized special register |

**Footer Note:**
The Xtensa processor has 64 internal AR registers. It is designed with the register windowing technique, so that the software can only access 16 of the 64 AR registers at any given time. The programming performance can be effectively improved by rotating windows, replacing function calls, and saving registers when exceptions are triggered.

**Document Footer:**
Espressif Systems
45 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback