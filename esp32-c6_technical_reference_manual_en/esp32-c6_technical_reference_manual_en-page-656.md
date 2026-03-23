

```markdown
Chapter 20 ECC Accelerator (ECC) GoBack


• ...

• write D[7] to "starting address + 28"

Note:
When the key size of 192 bits is used, you need to append 0 before 192 bits of data and write 256 bits of data.

20.3.2.4 Read Data

Read data means reading data from the starting address of an ECC memory block and using this data as the output from the ECC algorithm. To be specific, read data from an ECC memory block means reading D[n][31:0](n = 0, 1, … , 7) from the "starting address of this ECC memory block + 4 × n" successively:

• read D[0] from "starting address"
• read D[1] from "starting address + 4"
• ...
• read D[7] from "starting address + 28"

Note:
When the key size of 192 bits is used, only read the low 192 bits (6 blocks) of data.

20.3.2.5 Standard Calculation and Jacobian Calculation

ESP32-C6's ECC performs Base Point Calculation (including Base Point Verification and Base Point Multiplication) using the affine coordinates and Jacobian Calculation (including Jacobian Point Verification and Jacobian Point Multiplication) using the Jacobian coordinates.

20.4 Function Description

20.4.1 Key Size

ESP32-C6's ECC supports acceleration based on two key sizes (corresponding to two different elliptic curves). By configuring the ECC_MULT_KEY_LENGTH field, users can select the desired key size. For details, see Table 20.4-1 below.

Table 20.4-1. ECC Accelerator Key Size Selection

| ECC_MULT_KEY_LENGTH | Elliptic Curves* |
|---------------------|------------------|
| 1'b0                | FIPS P-192       |
| 1'b1                | FIPS P-256       |

* See definition of FIPS P-192 and P-256 in FIPS 186-3.
```