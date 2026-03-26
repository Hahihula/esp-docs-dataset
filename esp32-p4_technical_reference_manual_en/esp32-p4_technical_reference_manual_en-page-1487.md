

# Chapter 28 RSA Accelerator (RSA)

## Register 28.4. RSA_SET_START_MODMULT_REG (0x0810)

```
31
+---------------------------------------------------------------+
| (reserved)                                                   | 1 | 0 |
+---------------------------------------------------------------+
| Reset                                                       | 0 | 0 |
+---------------------------------------------------------------+
```

**RSA_SET_START_MODMULT** Configures whether or not to start the modular multiplication.

- O: No effect
- 1: Start
(WT)

## Register 28.5. RSA_SET_START_MULT_REG (0x0814)

```
31
+---------------------------------------------------------------+
| (reserved)                                                   | 1 | 0 |
+---------------------------------------------------------------+
| Reset                                                       | 0 | 0 |
+---------------------------------------------------------------+
```

**RSA_SET_START_MULT** Configures whether or not to start the multiplication.

- O: No effect
- 1: Start
(WT)

## Register 28.6. RSA_QUERY_IDLE_REG (0x0818)

```
31
+---------------------------------------------------------------+
| (reserved)                                                   | 1 | 0 |
+---------------------------------------------------------------+
| Reset                                                       | 0 | 0 |
+---------------------------------------------------------------+
```

**RSA_QUERY_IDLE** Represents the RSA status.

- O: Busy
- 1: Idle
(RO)