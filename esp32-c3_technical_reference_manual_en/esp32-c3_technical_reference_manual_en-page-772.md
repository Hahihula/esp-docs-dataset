

```markdown
| Action         | Internal state   | Note                |
|----------------|------------------|---------------------|
| Clear DTR      | RTS=?, DTR=0     | -                   |
| Clear RTS      | RTS=0, DTR=0     | Clear download flag |
| Set RTS        | RTS=1, DTR=0     | Reset SoC           |
| Clear RTS      | RTS=0, DTR=0     | Exit reset          |
```