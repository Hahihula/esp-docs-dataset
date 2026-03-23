

```markdown
TDM TX mode | In this mode, pulse code modulated (PCM) data is sent from memory via DMA, in a way of time division multiplexing (TDM). The signal lines include: BCK, WS, and DATA. Data up to 16 channels can be sent. TDM Philips standard, TDM MSB alignment standard, and TDM PCM standard are supported in this mode, depending on user configuration.
Normal PDM TX mode | In this mode, pulse density modulation (PDM) data is sent from memory via DMA. The signal lines include: WS and DATA. PDM standard is supported in this mode by user configuration.
PCM-to-PDM TX mode | In this mode, I2S as a master, converts the pulse code modulated (PCM) data from memory via DMA into pulse density modulation (PDM) data, and then sends the data out. Used signals: WS and DATA. PDM standard is supported in this mode by user configuration.
```

## 30.3 Features

The I2S module has the following features:

*   Master mode and slave mode
*   Full-duplex and half-duplex communications
*   Separate TX and RX units that can work independently or simultaneously
*   A variety of audio standards supported:
    *   TDM Philips standard
    *   TDM MSB alignment standard
    *   TDM PCM standard
    *   PDM standard
*   Configurable high-precision sample clock:
    *   Supports the following frequencies: 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz, and 192 kHz (Note that in slave mode, due to the frequency limitation of the clock source, the maximum sampling frequency is limited by the data bit width and number of channels. For detailed information, refer to Section 30.6)
*   8-/16-/24-/32-bit data communication
*   Direct Memory Access (DMA)
*   Standard I2S interface interrupts
```