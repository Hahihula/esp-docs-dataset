

```markdown
# Chapter 38

## Parallel IO Controller (PARL_IO)

### 38.1 Introduction

ESP32-C6 contains a Parallel IO controller (PARLIO) capable of transferring data between external devices and internal memory on a parallel bus through GDMA. It is composed of a TX unit and an RX unit, which are fixed as a transmitter and a receiver respectively. With the two units combined, PARLIO achieves full-duplex communication.

Due to its flexibility, PARLIO can function as a general interface to connect various peripherals. For example, with SPI as the master device and PARLIO as the slave device, a peer-to-peer transfer can be achieved. For detailed application examples, refer to Section 38.7.

### 38.2 Glossary

This section covers terminology used to describe the functionality of PARLIO.

| Term             | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| RX unit          | Module in PARLIO responsible for receiving data from external parallel bus and storing them into internal memory. |
| TX unit          | Module in PARLIO responsible for transmitting data from internal memory to external parallel bus. |
| RXD              | Parallel data received from the IO interface of the RX unit.                |
| TXD              | Parallel data sent from the IO interface of the TX unit.                    |
| Frame            | Transferred data unit from the moment the START signal is set to the moment the End of Frame (EOF) signal is received. |
| Free-running clock | Clock that toggles continuously. Otherwise, the clock only toggles during the period when valid data is received and remains constant for the rest of the time. |
| GDMA SUC EOF     | Signal that indicates GDMA successful end of frame. When GDMA receives this signal, a GDMA interrupt will be triggered, indicating that the current frame is correct and the receive is finished. |
| GDMA ERR EOF     | Signal that indicates GDMA error end of frame. When GDMA receives this signal, a GDMA interrupt will be triggered, indicating that the current frame has error and the receive is finished. |
| CDC              | Clock domain crossing.                                                      |

### 38.3 Features

The PARLIO module has the following main features:
```