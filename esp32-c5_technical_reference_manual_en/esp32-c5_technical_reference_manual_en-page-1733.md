

# Glossary

## Abbreviations for Peripherals

ADC ADC Controller  
AES AES (Advanced Encryption Standard) Accelerator  
CAN FD Controller Area Network Flexible Data-Rate  
DSA Digital Signature Algorithm  
ECC ECC (Elliptic Curve Cryptography) Accelerator  
ECDSA Elliptic Curve Digital Signature Algorithm  
eFuse eFuse Controller  
ETM Event Task Matrix  
GDMA GDMA (General Direct Memory Access) Controller  
HMAC HMAC (Hash-based Message Authentication Code) Accelerator  
I2C I2C (Inter-Integrated Circuit) Controller  
I2S I2S (Inter-IC Sound) Controller  
LEDC LED Control PWM (Pulse Width Modulation)  
MCPWM Motor Control PWM (Pulse Width Modulation)  
PARLIO Parallel IO Controller  
PCNT Pulse Count Controller  
PMS Permission Control  
RMT Remote Control Peripheral  
RNG Random Number Generator  
RSA RSA (Rivest Shamir Adleman) Accelerator  
SDIO SDIO Slave Controller  
SHA SHA (Secure Hash Algorithm) Accelerator  
SPI SPI (Serial Peripheral Interface) Controller  
TIMG Timer Group  
TRACE RISC-V Trace Encoder  
TSENS Temperature Sensor  
UART UART (Universal Asynchronous Receiver-Transmitter) Controller  
WDT Watchdog Timers  
XTS_AES External Memory Encryption and Decryption

## Abbreviations Related to Registers

REG Register.  
SYSREG System registers are a group of registers that control system reset, memory, clocks, software interrupts, power management, clock gating, etc.  
ISO Isolation. If a peripheral or other chip component is powered down, the pins, if any, to which its output signals are routed will go into a floating state. ISO registers isolate such pins and keep them at a certain determined value, so that the other non-powered-down peripherals/devices attached to these pins are not affected.