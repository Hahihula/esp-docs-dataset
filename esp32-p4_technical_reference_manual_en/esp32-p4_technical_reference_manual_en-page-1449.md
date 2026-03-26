

```markdown
## 26.3.2 Affine Coordinates and Jacobian Coordinates

An elliptic curve can be represented as below:

- In affine coordinates:
    $$y^2 = x^3 + ax + b \mod p$$

- In Jacobian coordinates:
    $$Y^2 = X^3 + aXZ^4 + bZ^6 \mod p$$

To convert affine coordinates $(x,y)$ to/from Jacobian coordinates $(X,Y,Z)$:

- From Jacobian to Affine coordinates:
    $$x = X/Z^2 \mod p$$
    $$y = Y/Z^3 \mod p$$

- From Affine to Jacobian coordinates:
    $$X = x$$
    $$Y = y$$
    $$Z = 1$$

## 26.3.3 Memory Blocks

ECC’s memory blocks store the input and output data of the ECC operation.

Table 26.3-1. ECC Accelerator Memory Blocks

| Memory Block          | Size (byte) | Starting Address* | Ending Address* | Access |
|-----------------------|-------------|-------------------|-----------------|--------|
| ECC_MULT_Mem_k        | 32          | 0x100             | 0x11F           | R/W    |
| ECC_MULT_Mem_Px       | 32          | 0x120             | 0x13F           | R/W    |
| ECC_MULT_Mem_Py       | 32          | 0x140             | 0x15F           | R/W    |
| ECC_MULT_Mem_Qx       | 32          | 0x160             | 0x17F           | R/W    |
| ECC_MULT_Mem_Qy       | 32          | 0x180             | 0x19F           | R/W    |
| ECC_MULT_Mem_Qz       | 32          | 0x1A0             | 0x1BF           | R/W    |

* Address offset related to the ECC accelerator base address is provided in Table 7.3-2 in Chapter 7 System and Memory.

## 26.3.4 Data and Data Block

ESP32-P4’s ECC can operate on 192-bit, 256-bit, or 384-bit data, depending on the elliptic curves.

For example, the 256-bit data $D[255:0]$ can be divided into eight 32-bit data blocks
$D[n][31:0] (n=0,1,\cdots,7)$. Data blocks with smaller indexes correspond to lower binary bits. To be specific:

$$D[255:0] = D[7][31:0], D[6][31:0], D[5][31:0], D[4][31:0], D[3][31:0], D[2][31:0], D[1][31:0], D[0][31:0]$$
```