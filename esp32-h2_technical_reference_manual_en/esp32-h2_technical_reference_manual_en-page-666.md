

```markdown
| ECDSA_WORK_MODE | Working Mode               |
|-----------------|----------------------------|
| 0               | Signature Verification     |
| 1               | Signature Generation       |

Table 25.4-2. ECDSA Elliptic Curves Selection

| ECDSA_ECC_CURVE | Elliptic Curve             |
|-----------------|----------------------------|
| 0               | P-192                      |
| 1               | P-256                      |

Table 25.4-3. ECDSA SHA Algorithm

| ECDSA_SHA_MODE | SHA Algorithm              |
|----------------|----------------------------|
| 1              | SHA-224                    |
| 2              | SHA-256                    |
| Others         | Invalid                    |

Table 25.4-4. ECDSA Working Status

| ECDSA_STATE_REG | Status   | Description                                                                                   |
|-----------------|----------|-----------------------------------------------------------------------------------------------|
| 0               | IDLE     | Idle or completed operation. Corresponding to IDLE Stage.                                    |
| 1               | LOAD     | Waiting for users to load information into ECDSA. Corresponding to LOAD Stage.                |
| 2               | GAIN     | Waiting for users to gain information from ECDSA. Corresponding to GAIN Stage.                |
| 3               | BUSY     | In the middle of a hardware operation. Corresponding to PREP, PROC & POST Stage.              |

## 25.4.2 Data and Data Block

ESP32-H2’s ECDSA accelerator operates on data of 256 or 512 bits. This data (D[255:0]) can be divided into 32-bit data blocks.

Take 256-bit long data as an example, D[n][31:0](n = 0, 1, … , 7). Data blocks with the smaller serial number correspond to the lower binary bits. To be specific:

D[255:0] = D[7][31:0], D[6][31:0], D[5][31:0], D[4][31:0], D[3][31:0], D[2][31:0], D[1][31:0], D[0][31:0]
```