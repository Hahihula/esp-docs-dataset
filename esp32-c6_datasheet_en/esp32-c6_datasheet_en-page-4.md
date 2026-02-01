**LP RISC-V processor:**
- Clock speed: up to 20 MHz
- Two stage pipeline

**General DMA controller, with 3 transmit channels and 3 receive channels**

**L1 cache:** 32 KB  
**ROM:** 320 KB  
**HP SRAM:** 512 KB  
**LP SRAM:** 16 KB  

**4096-bit eFuse memory, up to 1792 bits for users**

**Supported SPI protocols: SPI, Dual SPI, Quad SPI, QPI interfaces that allow connection to flash and other SPI devices off the chip's package**

**Flash controller with cache is supported**

**Flash in-Circuit Programming (ICP) is supported**

**Peripherals**
- 30 GPIOs (QFN40), or 22 GPIOs (QFN32)
  - 5 strapping GPIOs
  - 6 GPIOs needed for off-package flash

**Connectivity interfaces:**
- Two UARTs
- Low-power (LP) UART.
- Two SPI ports for communication with flash

**Power Management**
- Fine-resolution power control, including clock frequency, duty cycle, Wi-Fi operating modes, and individual internal component control  
- Four power modes designed for typical scenarios: Active, Modem-sleep, Light-sleep, Deep-sleep
- Power consumption in Deep-sleep mode is 7 µA

**Timers**
- 52-bit system timer
- Two 54-bit general-purpose timers
- Three digital watchdog timers  
- Analog watchdog timer

**Security**
- Secure boot - permission control on accessing internal and external memory
- Flash encryption - memory encryption and decryption
- Trusted execution environment (TEE) controller and access permission management (APM)
- Cryptographic hardware acceleration:
  - AES-128/256 (FIPS PUB 197)
  - ECC
  - HMAC
  - RSA

**Motor Control PWM (MCPWM)**  
**Remote control peripheral (TX/RX)**  
**Parallel IO interface (PARLIO)**  
**Event task matrix (ETM)**  

**Analog signal processing:**
- 12-bit SAR ADC, up to 7 channels  
- Temperature sensor

**Security**

**Espressif Systems**  
**Submit Documentation Feedback**  
**ESP32-C6 Series Datasheet v1.4**