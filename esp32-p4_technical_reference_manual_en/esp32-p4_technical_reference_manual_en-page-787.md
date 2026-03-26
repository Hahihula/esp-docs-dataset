

```markdown
Interrupt remapping allows software to redirect HP CPUx interrupts originally assigned to User Mode to a single specified Machine-mode interrupt. In this way, HP CPUx can indirectly respond to User-mode interrupts while running in Machine Mode.

Interrupt remapping features:

*   Enable interrupt remapping: Each peripheral interrupt source can be independently configured to participate in interrupt remapping. For example, setting `COREx_SOURCE_SRC_PASS_IN_SEC` to 1 enables interrupt remapping for interrupt matrix source `SOURCE`.

*   Specify the target Machine-mode interrupt: All remapped User-mode interrupt signals are uniformly mapped to the same specified Machine-mode interrupt. For example, writing a value n to `COREx_INTR_SIG_IDX_ASSERT_IN_SEC_REG` selects the Machine-mode interrupt with interrupt number n as the remapping target.

*   Access restrictions for remapping-related registers: the following registers and fields related to interrupt remapping are writable only when HP CPUx is operating in Machine Mode:

    -   `COREx_INTR_SIG_IDX_ASSERT_IN_SEC_REG`
    -   `COREx_SOURCE_SRC_PASS_IN_SEC`
    -   `COREx_SOURCE_SRC_IN_SEC_FLAG`

    -   When `COREx_SOURCE_SRC_IN_SEC_FLAG` is set to 1, `COREx_SOURCE_MAP` is also writable only in Machine Mode.

When interrupt source `SOURCE` has been mapped to the peripheral interrupt signal n of COREx, interrupt remapping for source `SOURCE` occurs only when all of the following conditions are met:

*   `COREx_SOURCE_SRC_PASS_IN_SEC` is set to 1
*   COREx is currently operating in Machine Mode
*   The peripheral interrupt signal n of COREx is internally delegated to User Mode by the CPU
*   The target interrupt signal specified by `COREx_INTR_SIG_IDX_ASSERT_IN_SEC_REG` is internally delegated to Machine Mode by the CPU
```