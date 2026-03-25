

```markdown
2. CONF: only used in DMA-controlled configurable segmented transfer. Set SPI_USR and SPI_USR_CONF to enable this state. If this state is not enabled, it means the current transfer is a single transfer.
3. PREP: prepare an SPI transaction and control SPI CS setup time. Set SPI_USR and SPI_CS_SETUP to enable this state.
4. CMD: send command sequence. Set SPI_USR and SPI_USR_COMMAND to enable this state.
5. ADDR: send address sequence. Set SPI_USR and SPI_USR_ADDR to enable this state.
6. DUMMY (wait cycle): send dummy sequence. Set SPI_USR and SPI_USR_DUMMY to enable this state.
7. DATA: transfer data.
  * DOUT: send data sequence. Set SPI_USR and SPI_USR_MOSI to enable this state.
  * DIN: receive data sequence. Set SPI_USR and SPI_USR_MISO to enable this state.
8. DONE: control SPI CS hold time. Set SPI_USR to enable this state.

Note:

To start this state machine, set SPI_USR first. SPI_MST_FD_WAIT_DMA_TX_DATA controls when SPI_USR takes effect:
  * 0: the configured state takes effect immediately after SPI_USR and other control registers are configured.
  * 1: if DOUT state is configured, the SPI_USR and other control registers will take effect, and the state machine will start, only when the data is ready in buf_tx_affifo.
```