

```markdown
## 38.5.9 Valid Signal Output of TX Unit

The TX unit can generate a valid signal aligned with TXD. Configure `PARL_IO_TX_VALID_OUTPUT_EN` to choose whether to output it to TXD. The polarity of the valid signal is fixed to active high.

The valid output function is disabled by default. When enabled, the output valid signal occupies the most significant bit (MSB) of the TXD, which means that no matter what the original value is, the 7th bit of TXD remains high and is output as the valid signal. However, the valid signal pin does not affect the bus width configuration. For example, if the data bus width is 1 bit, the valid output function can still be enabled with a fixed pin as `TXD[7]` while the data pin is `TXD[0]`.

**Note:**
When the valid signal output function and the clock gating function are enabled at the same time, the highest bit of TXD (i.e., the gating signal) is continuously at high level. In cases where software requires the bit not to continuously stay at high level, do not enable the two functions simultaneously.

## 38.5.10 Bus Idle Value of TX Unit

The TX unit is regarded as in idle state when it is not transmitting data. It supports a configurable bus idle value.

The bus idle value is `0x0` by default, and its maximum configurable value is `0xFF`. Note that the configured idle value should not conflict with other enabled functions. For example, when the MSB of TXD is used as the valid signal, users should avoid configuring the MSB of the idle value as 1.

## 38.5.11 Data Transfer in a Single Frame

The RX unit and the TX unit transfer data in the unit of bits, i.e., a single frame transfers 1 bit of data at least.

When the RX unit generates GDMA EOF signals through bit length, the maximum length of the single-frame transmission is `(2^19 - 1)` bits. When the RX unit generates GDMA EOF signals through the enable signal from an external device, there is no limit to the amount of bits of the single-frame transmission. The TX unit only generates GDMA EOF signals through bit length, so the maximum length of a single frame transmission is `(2^19 - 1)` bits.

Since PARLIO transfers data in the unit of bytes on the GDMA side, it will process the IO data when it is not aligned with the bytes.

* When receiving data, PARLIO will automatically pad `0` to the high bits of the data stored in memory via GDMA to make it aligned with bytes.
* When sending data, PARLIO will truncate the data retrieved from memory according to the configured value of `PARL_IO_TX_BITLEN`. Data exceeding the value will not be sent.

When the configured data bus width is 2/4/8-bit, the bit length must be configured as a multiple of the corresponding bus width.
```