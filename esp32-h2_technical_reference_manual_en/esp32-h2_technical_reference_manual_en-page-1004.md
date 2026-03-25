

```markdown
## 34.4.4.3 Frame Identifier

The Frame Identifier fields occupy two-byte (11-bit) long if the message is SFF, and four-byte (29-bit) long if the message is EFF.

The Frame Identifier fields for an SFF (11-bit) message are shown in Table 34.4-5 ~ 34.4-6.
```

```markdown
Table 34.4-5. TX/RX Identifier 1 (SFF); TWAII Address 0x44

| Bit 31-8 | Bit 7   | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|----------|---------|-------|-------|-------|-------|-------|-------|-------|
| Reserved | ID.10   | ID.9  | ID.8  | ID.7  | ID.6  | ID.5  | ID.4  | ID.3  |

Table 34.4-6. TX/RX Identifier 2 (SFF); TWAII Address 0x48

| Bit 31-8 | Bit 7   | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|----------|---------|-------|-------|-------|-------|-------|-------|-------|
| Reserved | ID.2    | ID.1  | ID.0  | X¹    | X²    | X²    | X²    | X²    |

Notes:

1. Don't care. Recommended to be compatible with receive buffer (i.e., set to RTR) in case of using the self-reception functionality (or together with self-test functionality).

2. Don't care. Recommended to be compatible with receive buffer (i.e., set to 0) in case of using the self-reception functionality (or together with self-test functionality).
```