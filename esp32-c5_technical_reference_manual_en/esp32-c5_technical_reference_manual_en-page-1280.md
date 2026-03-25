

```markdown
TDM TX mode    In this mode, pulse code modulated (PCM) data is sent in a way of time division multiplexing (TDM). The signal lines include BCK, WS, and DATA. Data up to 16 channels can be sent. TDM Philips standard, TDM MSB alignment standard, and TDM PCM standard are supported in this mode, depending on user configuration.

PDM TX mode    In this mode, pulse density modulation (PDM) data is sent. The signal lines include WS and DATA. PDM standard is supported in this mode by user configuration.

PCM-to-PDM Data Format Converter  A data format converter that converts PCM data into PDM data (hereinafter referred to as PCM-to-PDM converter), which can be enabled in PDM TX master mode. When the converter is enabled, I2S fetches pulse code modulated (PCM) data from storage via GDMA, converts it to pulse density modulation (PDM) data, and then transmits it.
```

## 35.3 Features

The I2S module has the following features:

*   Master mode and slave mode
*   Full-duplex and half-duplex communications
*   Separate TX and RX units that can work independently or simultaneously
*   A variety of audio standards supported:
    *   TDM Philips standard
    *   TDM MSB alignment standard
    *   TDM PCM standard
    *   PDM standard
*   Various TX/RX modes supported:
    *   TDM TX mode, up to 16 channels supported
    *   TDM RX mode, up to 16 channels supported
    *   PDM TX mode
        *   Raw PDM data transmission
        *   PCM-to-PDM data format conversion, up to 2 channels supported
    *   PDM RX mode
        *   Raw PDM data reception
*   Configurable clock source with frequencies up to 240 MHz
*   Configurable high-precision sample clock with a variety of sampling frequencies supported (refer to the note below for more details)
*   8/16/24/32-bit data width
```