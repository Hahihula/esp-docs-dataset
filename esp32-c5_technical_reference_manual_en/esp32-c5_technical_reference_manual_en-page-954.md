

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA)
GoBack

1. In this step, the software can also write the next message block to be processed, if any, in register ECDSA_MEM_M,
   while the interface starts SHA operation, to save time.
2. You are resuming the ECDSA SHA interface with the previously paused operation.

28.5.2 Clock

ECDSA uses two types of clocks:

- clk_ecdsa: function clock for ECDSA to operate
- clk_apb_ecdsa: bus clock used to configure ECDSA registers

Figure 28.5-2. clk_ecdsa Diagram

As shown in Figure 28.5-2 clk_ecdsa Diagram, the secure function source clock clk_sec_ori can be sourced from:

- XTAL_CLK
- RC_FAST_CLK
- PLL_F160M_CLK

ECDSA's function clock clk_ecdsa is configured by the clock gating register PCR_ECDASA_CLK_EN. When this register is set to 1, the clock gate is enabled, and clk_ecdsa is activated.

Figure 28.5-3. clk_apb_ecdsa Diagram
```