

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.109. LP_SYSTEM_IDBUS_ADDRHOLE_INFO_REG (0x019C)
```

```plaintext
(reserved)
┌───────────────────────────────────────────────────────────────────────────────┐
│ LP_SYSTEM_IDBUS_ADDRHOLE_SECURE | LP_SYSTEM_IDBUS_ADDRHOLE_WR | LP_SYSTEM_IDBUS_ADDRHOLE_ID |
└───────────────────────────────────────────────────────────────────────────────┘
```

```markdown
LP_SYSTEM_IDBUS_ADDRHOLE_ID Represents the LP CPU's ID value (00010) when ID-
BUS_ADDRHOLE_INT occurs. (RO)

LP_SYSTEM_IDBUS_ADDRHOLE_WR Represents the direction of transfer when ID-
BUS_ADDRHOLE_INT occurs. (RO)

LP_SYSTEM_IDBUS_ADDRHOLE_SECURE Represents the address hole type when ID-
BUS_ADDRHOLE_INT occurs. (RO)
```

```markdown
Register 20.110. LP_SYSTEM_RNG_DATA_REG (0x01A4)
```

```plaintext
LP_SYSTEM_RND_DATA
┌───────────────────────────────┐
│ 0x000000                    │ Reset
└───────────────────────────────┘
```

```markdown
LP_SYSTEM_RND_DATA Represents the RNG-generated random numbers. (RO)
```