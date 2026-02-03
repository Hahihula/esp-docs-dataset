**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**GoBack Link:** [GoBack](#)

**Section Note:**
- Set the corresponding bit in `GPIO_OUT_REG[31:0]` or `GPIO_OUT1_REG[21:0]` to the desired GPIO output value.

**Note Section:**
- `GPIO_OUT_REG[21:0]` and `GPIO_OUT_REG[31:26]` correspond to GPIO0 ~ 21 and GPIO26 ~ 31, respectively.
- `GPIO_OUT[25:22]` are invalid.
- `GPIO_OUT1_REG[16:0]` correspond to GPIO32 ~ 48, and `GPIO_OUT1_REG[21:17]` are invalid.

**Recommended Operation:** Use corresponding WITs and WITC registers such as `GPIO_OUT_WITs/GPIO_OUT_WITc` to set or clear the registers `GPIO_OUT_REG/GPIO_OUT1_REG`.

---

**Section Title:**
6.5.4 Sigma Delta Modulated Output

**Subsection 6.5.4.1 Functional Description**

**Body Text:**
Eight out of the 256 peripheral outputs (index: 93 ~ 100 in Table **6.11-1**) support 1-bit second-order sigma delta modulation. By default, output is enabled for these eight channels. This Sigma Delta modulator can also output PDM (pulse density modulation) signal with configurable duty cycle.

**Transfer Function Equation:**
\[ H(z) = X(z)z^{-1} + E(z)(1-z)^{-2} \]

E(z) represents quantization error and X(z) is the input. This modulator supports scaling down of APB_CLK by a divider 1 ~ 256:

- Set `GPIO_FUNCTION_CLK_EN` to enable the modulator clock.
- Configure `GPIO_SDn PRESCALE (n = 0 ~ 7 for eight channels)`.

After scaling, the clock cycle is equal to one pulse output cycle from the modulator. 

**Scaling Equation:**
\[ GPIO_SDn_IN \] is a signed number with a range of [-128, 127] and used to control the duty cycle \(^1\) of PDM output signal.

- `GPIO_SDn_IN = -128`, the duty cycle of the output signal is **0%**.
- `GPIO_SDn_IN = 0`, the duty cycle of the output signal nears about *50%*.
- `GPIO_SDn_IN = 127`, the duty cycle close to approximately around *100%*.

The formula for calculating PDM signal duty cycle is shown as below:

**Duty Cycle Formula:**
\[ Duty\_Cycle = \frac{GPIO_SDn_IN + 128}{256} \]

**Note Section (for PDM signals):**
For PDM signals, the duty cycle refers to percentage of high level cycles over a whole statistical period. For example:

- **Example:** 256 pulse cycles.

---

**Footer:**
Espressif Systems  
478 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback