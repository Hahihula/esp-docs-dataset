

```markdown
XTS_AES External Memory Encryption and Decryption

Abbreviations Related to Registers

REG Register.
SYSREG System registers are a group of registers that control system reset, memory, clocks, software interrupts, power management, clock gating, etc.
ISO Isolation. If a peripheral or other chip component is powered down, the pins, if any, to which its output signals are routed will go into a floating state. ISO registers isolate such pins and keep them at a certain determined value, so that the other non-powered-down peripherals/devices attached to these pins are not affected.
NMI Non-maskable interrupt is a hardware interrupt that cannot be disabled or ignored by the CPU instructions. Such interrupts exist to signal the occurrence of a critical error.
W1TS Abbreviation added to names of registers/fields to indicate that such register/field should be used to set a field in a corresponding register with a similar name. For example, the register GPIO_ENABLE_W1TS_REG should be used to set the corresponding fields in the register GPIO_ENABLE_REG.
W1TC Same as W1TS, but used to clear a field in a corresponding register.
```