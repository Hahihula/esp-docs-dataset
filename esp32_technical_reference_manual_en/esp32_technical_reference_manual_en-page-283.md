```markdown
### Table 14.3-3: AES-128 Key Endianness

| w[0] | w[1] | w[2] | w[3] |
|------|------|------|------|
| AES_KEY_3_REG(31:24) | AES_KEY_2_REG(31:24) | AES_KEY_1_REG(31:24) | AES_KEY_0_REG(31:24) |

AES_ENDIAN_REG[0] | 0
---|---
AES_ENDIAN_REG[0] | 0

AESENDORIAN_REG[0] | 0
---|---
AESENDORIAN_REG[0] | 1


AESENDORIAN_REG[0] | 1
---|---
AESENDORIAN_REG[0] | 1


### Table 14.3-4: AES-192 Key Endianness

| w[0] | w[1] | w[2] | w[3] |
|------|------|------|------|
| AES_KEY_4_REG(31:24) | AES_KEY_3_REG(31:24) | AES_KEY_2_REG(31:24) | AES_KEY_1_REG(31:24) |

AESENDORIAN_REG[0] | 0
---|---
AESENDORIAN_REG[0] | 0

AESENDORIAN_REG[0] | 1
---|---
AESENDORIAN_REG[0] | 1


### Table 14.3-5: AES-256 Key Endianness

| w[0] | w[1] | w[2] | w[3] |
|------|------|------|------|
| AES_KEY_8_REG(31:24) | AES_KEY_7_REG(31:24) | AES_KEY_6_REG(31:24) | AES_KEY_5_REG(31:24) |

AESENDORIAN_REG[0] | 0
---|---
AESENDORIAN_REG[0] | 0

AESENDORIAN_REG[0] | 1
---|---
AESENDORIAN_REG[0] | 1


```