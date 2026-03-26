

```markdown
## 26.4.2.11 Mod Division (Mod Div)

Mod Division can be represented as:

$$R = A \cdot B^{-1} \bmod N$$

where,

*   Input:
    -   A and B are stored in `ECC_MULT_Mem_Px` and `ECC_MULT_Mem_Py`.
    -   The value of N is related to the register fields below:
        *   `ECC_MULT_CURVE_MODE` to select the related curve.
        *   `ECC_MULT_MOD_BASE` to choose using mod base or order of the base point.
*   Output: R is stored in `ECC_MULT_Mem_Py`.

## 26.4.3 Enhancing Anti-Attack Performance

When performing different types of point multiplication calculations, i.e., mode 0, 3, 4, and 7, ESP32-P4's ECC accelerator offers an additional option to further enhance its anti-attack performance by ensuring that all point multiplication calculations take the same maximum runtime.

To enable the enhanced anti-attack performance, set `ECC_MULT_SECURITY_MODE` to 1. If this setting is enabled, each time the ECC accelerator perform a point multiplication calculation:

*   The execution latency is constant for a given operation.
*   Power consumption variations are minimized.

## 26.5 Clock and Reset

ESP32-P4's ECC only has one clock module (`CRYPTO_ECC_CLK`) and one reset module (`CRYPTO_ECC_RST`).

ECC's clock and reset is handled by the Power/Clock/Reset (PCR) module (see Chapter 10 *Reset and Clock* for more information). Users should enable the ECC clock by setting `HP_SYS_CLKRST_CRYPTO_ECC_CLK_EN` and release the ECC reset by clearing `HP_SYS_CLKRST_RST_EN_ECC` before starting the ECC accelerator. Besides, due to resource reuse between cryptography accelerator modules, users also need to additionally clear the `HP_SYS_CLKRST_RST_EN_ECDSA` bit.

## 26.6 Interrupts

ESP32-P4's ECC accelerator can generate the `ECC_INTR` interrupt signal that will be sent to the *Interrupt Matrix*.

`ECC_INTR` has only one interrupt source to generate the `ECC_INTR` interrupt signal, i.e., `ECC_MULT_CALC_DONE_INT`, which is triggered on the completion of an ECC calculation.
```