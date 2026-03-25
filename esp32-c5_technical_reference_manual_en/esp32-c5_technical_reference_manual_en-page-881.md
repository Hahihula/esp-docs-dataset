

```markdown
## 23.3.2 Affine Coordinates and Jacobian Coordinates

An elliptic curve can be represented as below:

* In affine coordinates:
    $$y^2 = x^3 + ax + b \mod p$$
* In Jacobian coordinates:
    $$Y^2 = X^3 + aXZ^4 + bZ^6 \mod p$$

To convert affine coordinates $(x,y)$ to/from Jacobian coordinates $(X,Y,Z)$:

* From Jacobian to Affine coordinates:
    $$x = X/Z^2 \mod p$$
    $$y = Y/Z^3 \mod p$$
* From Affine to Jacobian coordinates:
    $$X = x$$
    $$Y = y$$
    $$Z = 1$$

## 23.3.3 Memory Blocks

ECC’s memory blocks store the input and output data of the ECC operation.

Table 23.3-1. ECC Accelerator Memory Blocks

| Memory Block¹ | Size (byte) | Starting Address² | Ending Address² | Access |
|---------------|-------------|-------------------|-----------------|--------|
| ECC_MULT_Mem_k | 48          | 0x100             | 0x12F           | R/W    |
| ECC_MULT_Mem_Px | 48         | 0x130             | 0x15F           | R/W    |
| ECC_MULT_Mem_Py | 48         | 0x160             | 0x18F           | R/W    |
| ECC_MULT_Mem_Qx | 48         | 0x190             | 0x1BF           | R/W    |
| ECC_MULT_Mem_Qy | 48         | 0x1CO             | 0x1EF           | R/W    |
| ECC_MULT_Mem_Qz | 48         | 0x1FO             | 0x21F           | R/W    |

¹ The memory blocks store different types of data in different working modes. Refer to Section 23.4.2 for more details.
² Address offset related to the ECC accelerator base address is provided in Table 6.3-2 in Chapter 6 System and Memory.

## 23.3.4 Data and Data Block

ESP32-C5’s ECC can operate on 192-bit, 256-bit, or 384-bit data, depending on the elliptic curves.

For example, the 256-bit data $D[255:0]$ can be divided into eight 32-bit data blocks $D[n][31:0] (n=0,1,\cdots,7)$. Data blocks with smaller indexes correspond to lower binary bits. To be specific:

$$
D[255:0] = D[7][31:0], D[6][31:0], D[5][31:0], D[4][31:0], D[3][31:0], D[2][31:0], D[1][31:0], D[0][31:0]
$$
```