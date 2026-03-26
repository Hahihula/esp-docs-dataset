

```markdown
## 26.3.5 Writing Data

Writing data means writing data to an ECC memory block and using this data as the input to the ECC algorithm. To be specific, writing data to an ECC memory block means writing D[n][31:0](n = 0, 1, ..., 7) to the "starting address of this ECC memory block + 4 × n" sequentially:

- write D[0] to "starting address"
- write D[1] to "starting address + 4"
- ...
- write D[7] to "starting address + 28"

**Note:**
When storing data, write only the data block of the required length. Do not append a 0 to the most significant bit. For example, for 192-bit data, store only the 192 bits without appending 0.

## 26.3.6 Reading Data

Read data means reading data from the starting address of an ECC memory block and using this data as the output from the ECC algorithm. To be specific, read data from an ECC memory block means reading D[n][31:0](n = 0, 1, ..., 7) from the "starting address of this ECC memory block + 4 × n" successively:

- read D[0] from "starting address"
- read D[1] from "starting address + 4"
- ...
- read D[7] from "starting address + 28"

**Note:**
When reading data, only the data block of the required length needs to be read. For example, to read 192-bit data, simply read the lower 192 bits (i.e., 6 data blocks).

## 26.3.7 Standard Calculation and Jacobian Calculation

ESP32-P4's ECC performs Affine Point Calculation (including Affine Point Verification, Affine Point Add, and Affine Point Multiplication) using the affine coordinates and Jacobian Calculation (including Jacobian Point Verification, Jacobian Point Add, and Jacobian Point Multiplication) using the Jacobian coordinates.

## 26.4 Function Description

### 26.4.1 Curve Mode

ESP32-P4's ECC supports acceleration based on three curve modes, each corresponding to an elliptic curve. By configuring the ECC_MULT_CURVE_MODE field, users can select the desired key size. For details, see Table 26.4-1 below.
```