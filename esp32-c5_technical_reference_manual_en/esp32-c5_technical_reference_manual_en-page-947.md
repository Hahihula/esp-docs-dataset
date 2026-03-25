

```markdown
| ECDSA_WORK_MODE | Working Mode               |
|-----------------|----------------------------|
| 0               | Signature Verification     |
| 1               | Signature Generation        |
| 2               | Public Key Export           |

Table 28.4-2. ECDSA Elliptic Curves Selection

| ECDSA_ECC_CURVE | Elliptic Curve             |
|-----------------|----------------------------|
| 0               | P-192                      |
| 1               | P-256                      |
| 2               | P-384                      |

Table 28.4-3. ECDSA SHA Algorithm

| ECDSA_SHA_MODE | SHA Algorithm             |
|----------------|---------------------------|
| 1              | SHA-224                   |
| 2              | SHA-256                   |
| 3              | SHA-384                   |
| 4              | SHA-512                   |
| 5              | SHA-512-224               |
| 6              | SHA-512-256               |
| Others         | Invalid                   |

Table 28.4-4. ECDSA Working State

| ECDSA_STATE_REG | State   | Description                                                                                      |
|-----------------|---------|--------------------------------------------------------------------------------------------------|
| 0               | IDLE    | Idle or completed operation. Corresponding to IDLE stage.                                        |
| 1               | LOAD    | Waiting for users to load information into ECDSA. Corresponding to LOAD stage.                   |
| 2               | GAIN    | Waiting for users to gain information from ECDSA. Corresponding to GAIN stage.                   |
| 3               | BUSY    | In the middle of a hardware operation. Corresponding to PREP, PROC, and POST stage.              |
```