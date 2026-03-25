

```markdown
Chapter 23 ECC Accelerator (ECC)

GoBack

Figure 23.4-1. clk_ecc Diagram

As shown in Figure 23.4-1 clk_ecc Diagram, the secure function source clock clk_sec_ori can be sourced from:

*   XTAL_CLK
*   RC_FAST_CLK
*   PLL_F160M_CLK

ECC's function clock clk_ecc is configured by the clock gating register PCR_ECC_CLK_EN. When this register is set to 1, the clock gate is enabled, and clk_ecc is activated.

Figure 23.4-2. clk_apb_ecc Diagram

As shown in Figure 23.4-2 clk_apb_ecc Diagram, ECC's configuration clock clk_apb_ecc can be sourced from SYSTEM_APB_CLK.

ECC's configuration clock clk_apb_ecc is controlled by the clock gating register PCR_ECC_CLK_EN. When this register is set to 1, the clock gate is enabled, and clk_apb_ecc is activated.

For more information about clocks, see Section 9 Reset and Clock.

23.4.5 Reset

The ECC module supports two types of resets:

*   Full self-reset: Write 1 and then 0 to PCR_ECC_RST_EN to reset the entire ECC module.
```