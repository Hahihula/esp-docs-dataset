

```markdown
unusable.

Neither the program memory nor the LUT RAM are accessible to the main processor directly. Rather, they need to be written indirectly, by setting an address in one register and then writing the data in a second register.

Specifically, for the LUT RAM, the address is written in the BITSCRAMBLER_TX_LUT_IDX field of BITSCRAMBLER_TX_LUT_CFG0_REG and the data is written to or read from BITSCRAMBLER_TX_LUT_CFG1_REG. The width of the LUT, as visible to the BitScrambler, can be configured using the BITSCRAMBLER_TX_LUT_MODE field. Note that when the host processor writes to the LUT in the aforementioned fashion, the addressing and data size needs to adhere to the configured LUT width.

Similarly, the instruction memory is written by setting the address up in BITSCRAMBLER_TX_INST_CFG0_REG and writing the data to or reading it from BITSCRAMBLER_TX_INST_CFG1_REG. As the BitScrambler instructions are 257 bits, one instruction needs to be written as 9 32-bit words (with the 257th bit being in the LSB of the 9th word). To achieve that purpose, the BITSCRAMBLER_TX_INST_CFG0_REG register is divided into two fields. The position of the instruction is written into the BITSCRAMBLER_TX_INST_IDX field while the word offset within the instruction is written to BITSCRAMBLER_TX_INST_POS.

As the BitScrambler has the ability to generate more or less data than it gets on the input, a BitScrambler-controlled DMA stream can end in one or two ways. The first is that the receiver (either memory in case of the RX BitScrambler, or the peripheral in case of the TX BitScrambler) stops accepting data because it is configured to only receive a limited number of bytes. This case is pretty simple: the BitScrambler will simply halt as it cannot write any more data. The other way is that the transmitter (the peripheral for the RX BitScrambler and the memory for the TX BitScrambler) stops sending data. This is a more complicated situation, as the BitScrambler may or may not be processing some data that needs to be written to the output.

In order to allow the BitScrambler to send out the data it is still processing, two methods have been devised to handle a certain amount of data after the input data stream has ended. Both depend on setting BITSCRAMBLER_RX_TAILING_BITS_REG to a certain value N:

* EOF-on-N-reads: After the input data stream ends, the BitScrambler reads N dummy bytes from the input. The value of these bytes is zero. After the Nth byte is read, the BitScrambler halts and the DMA stream ends.
* EOF-on-N-writes: After the input data stream ends, the BitScrambler is allowed to write N more bytes to the output. During this time, any reads on the input stream return zero-value dummy bytes. After the N'th byte is written, the BitScrambler halts and the DMA stream ends.

To configure either mode, set the option bits as follows:

Table 44.5-12. Settings for EOF modes

| Register                        | EOF-on-N-reads | EOF-on-N-writes |
|----------------------------------|----------------|-----------------|
| BITSCRAMBLER_TX_RD_DUMMY         | 1              | 1               |
| BITSCRAMBLER_TX_FETCH_MODE       | 0              | 0               |
| BITSCRAMBLER_TX_EOF_MODE         | 1              | 0               |
| BITSCRAMBLER_TX_HALT_MODE        | 1              | 1               |
```