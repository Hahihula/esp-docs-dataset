

```markdown
Register 2.78. pmcfg2 (0x3A1)

pm9cfg    pmp8cfg     pmp7cfg      pmp6cfg
          |             |             |
          +-------------+-------------+
        31   24   23   16   15   8   7   0

[31:24] [23:16] [15:8] [7:0]

0         0         0         0       Reset

pmcfg Configuration register for PMP entry 11. (R/W)
pmp10cfg Configuration register for PMP entry 10. (R/W)
pmp9cfg Configuration register for PMP entry 9. (R/W)
pmp8cfg Configuration register for PMP entry 8. (R/W)

Register 2.79. pmcfg3 (0x3A2)

pm15cfg   pmp14cfg    pmp13cfg     pmp12cfg
          |             |             |
          +-------------+-------------+
        31   24   23   16   15   8   7   0

[31:24] [23:16] [15:8] [7:0]

0         0         0         0       Reset

pmp15cfg Configuration register for PMP entry 15. (R/W)
pmp14cfg Configuration register for PMP entry 14. (R/W)
pmp13cfg Configuration register for PMP entry 13. (R/W)
pmp12cfg Configuration register for PMP entry 12. (R/W)

The PMP configuration register format for any PMP entry is shown as follows.
```