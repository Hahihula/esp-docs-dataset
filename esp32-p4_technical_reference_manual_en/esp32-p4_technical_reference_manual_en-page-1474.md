

```markdown
Chapter 27 HMAC Accelerator (HMAC)

Register 27.6. HMAC_SET_RESULT_FINISH_REG (0x005C)
```

```markdown
HMAC_SET_RESULT_END Configures whether to exit upstream mode and clear calculation results.
O: Not exit
1: Exit upstream mode and clear calculation results.
(WO)
```

```markdown
Register 27.7. HMAC_SET_INVALIDATE_JTAG_REG (0x0060)
```

```markdown
HMAC_SET_INVALIDATE_JTAG Configures whether or not to clear calculation results when re-enabling JTAG in downstream mode.
O: Not clear
1: Clear calculation results
(WO)
```