

```markdown
## 20.3.5 Writing Data

Writing data means writing data to an ECC memory block and using this data as the input to the ECC algorithm. To be specific, writing data to an ECC memory block means writing D[n][31:0](n = 0, 1, ··· , 7) to the "starting address of this ECC memory block + 4 × n" successively:

- write D[0] to "starting address"
- write D[1] to "starting address + 4"
- ...
- write D[7] to "starting address + 28"

**Note:**
When the key size of 192 bits is used, append 0 before 192 bits of data to ensure 256-bit data is written.

## 20.3.6 Reading Data

Reading data means reading data from the starting address of an ECC memory block and using this data as the output from the ECC algorithm. To be specific, reading data from an ECC memory block means reading D[n][31:0](n = 0, 1, ··· , 7) from the "starting address of this ECC memory block + 4 × n" successively:

- read D[0] from "starting address"
- read D[1] from "starting address + 4"
- ...
- read D[7] from "starting address + 28"

**Note:**
When the key size of 192 bits is used, only read the low 192 bits (6 blocks) of data.

## 20.3.7 Standard Calculation and Jacobian Calculation

ESP32-C61's ECC performs Affine Point Calculation (including Affine Point Verification, Affine Point Add, and Affine Point Multiplication) using the affine coordinates and Jacobian Calculation (including Jacobian Point Verification, Jacobian Point Add, and Jacobian Point Multiplication) using the Jacobian coordinates.

## 20.4 Function Description

### 20.4.1 Key Size

ESP32-C61's ECC supports acceleration based on two key sizes, each corresponding to an elliptic curve. By configuring the ECC_MULT_KEY_LENGTH field, users can select the desired key size. For details, see Table 20.4-1 below.
```