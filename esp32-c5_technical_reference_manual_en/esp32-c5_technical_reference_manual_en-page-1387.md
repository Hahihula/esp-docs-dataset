

```markdown
| TWAIFD_RTRTH | TWAIFD_RTRLLE | Behavior                                                                 |
|--------------|---------------|---------------------------------------------------------------------------|
| -            | 0             | Frame transmission is attempted without any limitation (until it is successful or unit turns bus-off). |
| 0            | 1             | Frame transmission is attempted only once, there are no retransmission attempts after first failed transmission (so-called one shot mode). |
| 1 - 15       | 1             | Frame transmission is attempted TWAIFD_RTRTH + 1 times (initial transmission + TWAIFD_RTRTH retransmissions). |
```