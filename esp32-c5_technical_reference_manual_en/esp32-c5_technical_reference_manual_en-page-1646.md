

```markdown
because when the control source is the DMA output data, the gating signal is fixed to the MSB of TXD. The clock signal can be toggled when this bit is at a high level. Note that when selecting DMA output data as the control source, if the peripheral is in an idle state, the clock gating will be controlled by the MSB of the user-configured bus idle value. For configuration guidelines, refer to Section 43.5.10 Bus Idle Value of TX Unit. When the gating function is enabled while using DMA output data as the control source, there are at most 7 IO pins left usable for TXD as the gating signal occupies one IO.

Set `PARL_IO_TX_VALID_OUTPUT_EN` to 1 to select the chip select signal (CS) as the control source. In this case, there is no limit to the bit width.

## 43.5.10 Bus Idle Value of TX Unit

The TX unit is regarded as in idle state when it is not transmitting data. It supports a configurable bus idle value.

Note that the configured idle value should not conflict with other enabled functions. For example, when the MSB of TXD is used as the valid signal, users should avoid configuring the MSB of the idle value as 1.

## 43.5.11 Data Transfer in a Single Frame

The RX unit and the TX unit transfer data in the unit of bits, i.e., a single frame transfers 1 bit of data at least.

When the RX unit generates GDMA EOF signals through bit length, the maximum length of the single-frame transmission is (2¹⁹ − 1) bits. When the RX unit generates GDMA EOF signals through the enable signal from an external device, there is no limit to the amount of bits of the single-frame transmission.

The TX unit only generates GDMA EOF signals through byte length, so the maximum length of a single frame transmission is (2¹⁹ − 1) bytes.

Since PARLIO transfers data in the unit of bytes on the GDMA side, it will process the IO data when it is not aligned with the bytes.

* When receiving data, PARLIO will automatically pad 0 to the high bits of the data stored in memory via GDMA to make it aligned with bytes.
* When sending data, PARLIO will truncate the data retrieved from memory according to the configured value of `PARL_IO_TX_BITLEN`. Data exceeding the value will not be sent.

When the configured data bus width is 2/4/8-bit, the bit length must be configured as a multiple of the corresponding bus width.

## 43.5.12 Bit Reversal in One Byte

The sequence of data within one byte can be reversed when data bus width is 1/2/4-bit. Taking the RX unit as an example, when the configured bus width is 2 bits, the data needs to be packed into one byte before being written into the RX FIFO.

Presume that the original bit sequence is:

```
{ {b₀, b₁}, {b₂, b₃}, {b₄, b₅}, {b₆, b₇} }
```

If the bit reversal is enabled, the sequence will be reordered to:
```