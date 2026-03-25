

```markdown
Chapter 25 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


Register 25.4. ECDSA_INT_RAW_REG (0x0000)

31 | Reset
   | 2 | 1 | 0
   +---+---+---+
   |   |   |   |
(reserved)
   |   |   |   |

ECDSA_CALC_DONE_INT_RAW The raw interrupt status of the ECDSA_CALC_DONE_INT interrupt.
(RO/WTC/SS)

ECDSA_SHA_RELEASE_INT_RAW The raw interrupt status of the ECDSA_SHA_RELEASE_INT inter-
rupt. (RO/WTC/SS)


Register 25.5. ECDSA_INT_ST_REG (0x0010)

31 | Reset
   | 2 | 1 | 0
   +---+---+---+
   |   |   |   |
(reserved)
   |   |   |   |

ECDSA_CALC_DONE_INT_ST The masked interrupt status of the ECDSA_CALC_DONE_INT inter-
rupt. (RO)

ECDSA_SHA_RELEASE_INT_ST The masked interrupt status of ECDSA_SHA_RELEASE_INT inter-
rupt. (RO)
```