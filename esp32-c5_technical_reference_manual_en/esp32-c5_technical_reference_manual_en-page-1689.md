

```markdown
Register 44.14. BITSCRAMBLER_TX_STATE_REG (0x0030)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 31        | BITS                        | Reserved                                                                     |
| 30        | TX_EOF_TRACE_CLR             | Represents whether BitScrambler TX path is halted.                           |
| 29        | TX_EOF_OVERLOAD              | O: Not halted                                                                |
|           |                              | 1: Halted                                                                    |
|           | (RO)                          |                                                                             |
| 16..0     | TX_EOF_GET_CNT               | Represents whether BitScrambler TX path is running.                          |
|           | O: Not running                 | 1: Running                                                                   |
|           | (RO)                          |                                                                             |
|           | TX_IN_WAIT                   | Represents whether BitScrambler TX path is waiting for write back done.      |
|           | O: Not waiting                | 1: Waiting                                                                   |
|           | (RO)                          |                                                                             |
|           | TX_IN_PAUSE                  | Represents whether BitScrambler TX path is paused.                           |
|           | O: Not paused                 | 1: Paused                                                                    |
|           | (RO)                          |                                                                             |
|           | TX_FIFO_EMPTY                | Represents whether BitScrambler TX FIFO is empty                            |
|           | O: Not empty                  | 1: Empty                                                                     |
|           | (RO)                          |                                                                             |
|           | TX_EOF_GET_CNT               | Represents byte count of BitScrambler TX path after EOF is received.        |
|           | (RO)                          |                                                                             |
|           | TX_EOF_OVERLOAD              | Represents whether BitScrambler TX path tries to process more than one EOF.  |
|           | O: Not try to process more than one EOF | 1: Try to process more than one EOF                                       |
|           | (RO)                          |                                                                             |
|           | TX_EOF_TRACE_CLR             | Configures whether to clear BITS, TX_EOF_OVERLOAD and TX_EOF_GET_CNT.        |
|           | O: Not clear                  | 1: Clear                                                                     |
|           | (WT)                          |                                                                             |

```
```plaintext
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE       TX_FIFO_EMPTY
TX_IN_WAIT                   TX_IN_PAUSE        TX_IN_RUN         TX_EOF_GET_CNT
TX_IN_RUN                    TX_IN_PAUSE        TX_IN_WAIT        TX_EOF_OVERLOAD
TX_EOF_GET_CNT               TX_EOF_OVERLOAD    TX_EOF_TRACE_CLR   (reserved)
```

```markdown
BITS                        TX_EOF_TRACE_CLR    TX_EOF_OVERLOAD   TX_EOF_GET_CNT
TX_IN_IDLE                   TX_IN_RUN          TX_IN_PAUSE