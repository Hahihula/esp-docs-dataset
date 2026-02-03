**Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

### 2.5.2.6 JUMPS – Jump to a Relative Address (Conditional upon Stage Count Register)

#### Operand | Description - see Figure 2.5-13
---|---
Threshold | Threshold value for condition (see Cond below) to jump
Cond | Condition to jump:
- 0 - jump if RO < Threshold
- 1 - jump if RO > Threshold
- 2 - jump if RO = Threshold

#### Step 
Relative shift from current position, expressed in 32-bit words:  
if Step[7] = 0, then PC = PC + Step[6:0]  
if Step[7] = 1, then PC = PC - Step[6:0]

**Note:** All jump addresses are expressed in 32-bit words.

#### Description
The instruction executes a jump to a relative address if the condition is true. The condition is the result of comparing the RO register value and the Threshold value.

---

### Figure 2.5-13. Instruction Type - JUMPS

| Step | Cond |
|------|------|
| 8    | 0     |
|      | 2     |

**Operand | Description - see Figure 2.5-13**
---|---
Threshold | Threshold value for condition (see Cond below) to jump
Cond | Condition to jump:
- 1X - jump if Stage_cnt <= Threshold
- OO - jump if Stage_cnt < Threshold
- O1 - jump if Stage_cnt >= Threshold

#### Step 
Relative shift from current position, expressed in 32-bit words:  
if Step[7] = 0, then PC = PC + Step[6:0]  
if Step[7] = 1, then PC = PC - Step[6:0]

**Note:**  
- For more information about the stage count register, please refer to Section **2.5.2.1**.
- All jump addresses are expressed in 32-bit words.

#### Description
The instruction executes a jump to a relative address if the condition is true. The condition itself is the result of comparing the value of Stage_cnt (stage count register) and the Threshold value.

---

### 2.5.2.7 HALT – End the Program

**Espressif Systems**  
**318 ESP32-S3 TRM (Version 1.7)**  

[Submit Documentation Feedback](#)