

```markdown
Chapter 23 ECC Accelerator (ECC)

GoBack

23.4.2.11 Mod Division (Mod Div)
Mod Division can be represented as:
R = A · B⁻¹ mod N

where,
• Input:
    – A and B are stored in ECC_MULT_Mem_Px and ECC_MULT_Mem_Py.
    – The value of N is related to the register fields below:
        * ECC_MULT_CURVE_MODE to select the related curve.
        * ECC_MULT_MOD_BASE to choose using mod base or order of the base point.
• Output: R is stored in ECC_MULT_Mem_Py.

23.4.3 Enhancing Anti-Attack Performance
When performing different types of point multiplication calculations, i.e., mode 0, 3, 4, and 7, ESP32-C5’s ECC accelerator offers an additional option to further enhance its anti-attack performance by ensuring that all point multiplication calculations take the same maximum runtime.

To enable the enhanced anti-attack performance, set ECC_MULT_SECURITY_MODE to 1. If this setting is enabled, each time the ECC accelerator perform a point multiplication calculation:
• The execution latency is constant for a given operation.
• Power consumption variations are minimized.

23.4.4 Clock
ECC uses two types of clocks:
• clk_ecc: function clock for ECC to operate
• clk_apb_ecc: bus clock used to configure ECC registers
```