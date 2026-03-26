

```markdown
| ECDSA_ECC_CURVE | Elliptic Curve |
|-----------------|----------------|
| 0               | P-192          |
| 1               | P-256          |
| 2               | P-384          |

Table 31.4-2. ECDSA_DS SHA Algorithm

| ECDSA_SHA_MODE | SHA Algorithm   |
|----------------|-----------------|
| 1              | SHA-224         |
| 2              | SHA-256         |
| 3              | SHA-384         |
| 4              | SHA-512         |
| 5              | SHA-512-224     |
| 6              | SHA-512-256     |
| Others         | Invalid         |

Table 31.4-3. ECDSA_DS Working State

| ECDSA_STATE_REG | State   | Description                                                                                   |
|-----------------|---------|-----------------------------------------------------------------------------------------------|
| 0               | IDLE    | Idle or completed operation. Corresponding to IDLE Stage.                                     |
| 1               | LOAD    | Waiting for users to load information into ECDSA_DS. Corresponding to LOAD Stage.             |
| 2               | Reserved| –                                                                                             |
| 3               | BUSY    | In the middle of a hardware operation. Corresponding to PREP, PROC & POST Stage.              |

## 31.4.2 Data and Data Block

ESP32-P4's ECDSA_DS module can operate on data of 192, 256, 384, or 512 bits. For example, the data (D[255:0]) can be divided into 32-bit data blocks.

Take 256-bit long data as an example, D[n][31:0](n = 0, 1, …, 7). Data blocks with the smaller serial number correspond to the lower binary bits. To be specific:

D[255:0] = D[7][31:0], D[6][31:0], D[5][31:0], D[4][31:0], D[3][31:0], D[2][31:0], D[1][31:0], D[0][31:0]
```