

```markdown
Register 40.9. CSI_HOST_SCRAMBLING_REG (0x0300)

CSI_HOST_SCRAMBLE_ENABLE   Configures whether to enable the descrambler.
    0: Disable
    1: Enable
(R/W)
```

```markdown
Register 40.10. CSI_HOST_SCRAMBLING_SEEDn_REG (n: 1-2) (0x0300 + 0x04*n)

CSI_HOST_SCRAMBLE_SEED_LANE(n-1)   Configures the seed value used by the descrambler for lane
    n-1. (R/W)
```