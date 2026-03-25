

```markdown
| Action          | Internal state   | Note                     |
|-----------------|------------------|--------------------------|
| Clear DTR       | RTS=?, DTR=0     | Initialize to known values |
| Clear RTS       | RTS=0, DTR=0    | -                        |
| Set DTR         | RTS=0, DTR=1    | Set download mode flag   |
| Clear RTS       | RTS=0, DTR=1    | Propagate DTR            |
| Set RTS         | RTS=1, DTR=1    | -                        |
| Clear DTR       | RTS=1, DTR=0    | Reset SoC                |
| Set RTS         | RTS=1, DTR=0    | Propagate DTR            |
| Clear RTS       | RTS=0, DTR=0    | Clear download flag      |

To reset the SoC into booting from flash:

Table 37.5-2. Reset SoC into Booting from flash

| Action          | Internal state   | Note                     |
|-----------------|------------------|--------------------------|
| Clear DTR       | RTS=?, DTR=0     | -                        |
| Clear RTS       | RTS=0, DTR=0    | Clear download flag      |
| Set RTS         | RTS=1, DTR=0    | Reset SoC                |
| Clear RTS       | RTS=0, DTR=0    | Exit reset               |
```