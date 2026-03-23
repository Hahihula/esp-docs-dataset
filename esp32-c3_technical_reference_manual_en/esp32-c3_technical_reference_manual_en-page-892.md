

# Glossary

## Abbreviations for Peripherals

| AES | AES (Advanced Encryption Standard) Accelerator |
| DS | Digital Signature |
| DMA | DMA (Direct Memory Access) Controller |
| eFuse | eFuse Controller |
| HMAC | HMAC (Hash-based Message Authentication Code) Accelerator |
| I2C | I2C (Inter-Integrated Circuit) Controller |
| I2S | I2S (Inter-IC Sound) Controller |
| LEDC | LED Control PWM (Pulse Width Modulation) |
| RMT | Remote Control Peripheral |
| RNG | Random Number Generator |
| RSA | RSA (Rivest Shamir Adleman) Accelerator |
| SHA | SHA (Secure Hash Algorithm) Accelerator |
| SPI | SPI (Serial Peripheral Interface) Controller |
| SYSTIMER | System Timer |
| TIMG | Timer Group |
| TWAI | Two-wire Automotive Interface |
| UART | UART (Universal Asynchronous Receiver-Transmitter) Controller |
| WDT | Watchdog Timers |

## Abbreviations Related to Registers

| REG | Register. |
| SYSREG | System registers are a group of registers that control system reset, memory, clocks, software interrupts, power management, clock gating, etc. |
| ISO | Isolation. If a peripheral or other chip component is powered down, the pins, if any, to which its output signals are routed will go into a floating state. ISO registers isolate such pins and keep them at a certain determined value, so that the other non-powered-down peripherals/devices attached to these pins are not affected. |
| NMI | Non-maskable interrupt is a hardware interrupt that cannot be disabled or ignored by the CPU instructions. Such interrupts exist to signal the occurrence of a critical error. |
| W1TS | Abbreviation added to names of registers/fields to indicate that such register/field should be used to set a field in a corresponding register with a similar name. For example, the register GPIO_ENABLE_W1TS_REG should be used to set the corresponding fields in the register GPIO_ENABLE_REG. |
| W1TC | Same as W1TS, but used to clear a field in a corresponding register. |

## Access Types for Registers

Sections *Register Summary* and *Register Description* in TRM chapters specify access types for registers and their fields.

Espressif Systems
892
ESP32-C3 TRM (Version 1.3)

Submit Documentation Feedback