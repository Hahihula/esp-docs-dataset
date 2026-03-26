

```markdown
To enable larger single-frame transmissions, set `PARL_IO_TX_EOF_GEN_SEL` to 1. In this mode, the hardware uses the EOF configured in the GDMA inlink list as the end-of-transmission signal for a single frame. As a result, data transmission is no longer constrained by the bit width of `PARL_IO_TX_BITLEN`, allowing for significantly larger data frames.

## 58.5.9 TX Chip Select Function

To emulate the LCD I8080 protocol, the TX unit is equipped with an output chip select (CS) signal, which is active low. Configure `PARL_IO_TX_CS_START_DELAY` and `PARL_IO_TX_CS_STOP_DELAY` to control the phase relationship between the GDMA output data and the CS signal. Note that when clock gating is enabled and the CS signal is used as the control source for clock gating, configuring these two registers not only implements the basic function, but also allows control over the phase relationship between the output clock and the CS signal.

## 58.5.10 Output Clock Gating of TX Unit

The TX unit supports output clock gating. The clock gating function is disabled by default, and can be enabled by software via setting `PARL_IO_TX_GATING_EN`.

Currently, the most significant bit (MSB) of TXD can be configured to be controlled by one of two sources: GDMA output data or the chip select signal (CS). Set `PARL_IO_TX_VALID_OUTPUT_EN` to 0 to select the GDMA output data as the control source. In this case, the TX unit must be configured with the maximum bit width, because when the control source is the GDMA output data, the gating signal is fixed to the MSB of TXD. The clock signal can be toggled when this bit is at a high level. Note that when selecting GDMA output data as the control source, if the peripheral is in an idle state, the clock gating will be controlled by the MSB of the user-configured bus idle value. For configuration guidelines, refer to Section 58.5.11 Bus Idle Value of TX Unit.

When the gating function is enabled while using GDMA output data as the control source, there are at most 15 IO pins left usable for TXD as the gating signal occupies one IO.

Set `PARL_IO_TX_VALID_OUTPUT_EN` to 1 to select the chip select signal (CS) as the control source. In this case, there is no limit to the bit width.

## 58.5.11 Bus Idle Value of TX Unit

The TX unit is regarded as in idle state when it is not transmitting data. It supports a configurable bus idle value.

The bus idle value is 0x0 by default, and its maximum configurable value is 0xFF. Note that the configured idle value should not conflict with other enabled functions. For example, when the MSB of TXD is used as the valid signal, users should avoid configuring the MSB of the idle value as 1.

## 58.5.12 Data Transfer in a Single Frame

The RX unit and the TX unit transfer data in the unit of bits, i.e., a single frame transfers 1 bit of data at least.

When the RX unit generates GDMA EOF signals through bit length, the maximum length of the single-frame transmission is (2^19 – 1) bits. When the RX unit generates GDMA EOF signals through the enable signal from an external device, there is no limit to the amount of bits of the single-frame transmission.
```