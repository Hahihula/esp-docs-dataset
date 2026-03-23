

```markdown
Chapter 20 RSA Accelerator (RSA)

Register 20.8. RSA_CLEAR_INTERRUPT_REG (0x081C)

31
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
RSA_CLEAR_INTERRUPT

RSA_CLEAR_INTERRUPT Set this bit to 1 to clear the RSA interrupts. (W/O)

Register 20.9. RSA_CONSTANT_TIME_REG (0x0820)

31
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
RSA_CONSTANT_TIME

RSA_CONSTANT_TIME_REG Controls the constant_time option. 0: acceleration. 1: no acceleration (by default). (R/W)

Register 20.10. RSA_SEARCH_ENABLE_REG (0x0824)

31
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset
RSA_SEARCH_ENABLE

RSA_SEARCH_ENABLE Controls the search option. 0: no acceleration (by default). 1: acceleration. (R/W)
```