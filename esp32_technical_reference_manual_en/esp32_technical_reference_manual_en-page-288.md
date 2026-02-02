**Title: Chapter 15 RSA Accelerator (RSA)**

**Body Text:**
To represent numbers used as operands, define a base-b positional notation:

\[ b = 2^{32} \]

In this notation, each number is represented by a sequence of base-b digits. Each digit in the representation can be any integer from \(0\) to \(b-1\). Representing an N-bit number requires n base-b digits (all possible lengths are multiples of 32).

\[ 
n = \frac{N}{32} \\
Z = (Z_{n-1} Z_{n-2} \cdots Z_0)_b \\
X = (X_{n-1} X_{n-2} \cdots X_0)_b \\
Y = (Y_{n-1} Y_{n-2} \cdots Y_0)_b \\
M = (M_{n-1} M_{n-2} \cdots M_0)_b \\
\overline{r} = (\overline{r}_{n-1} \overline{r}_{n-2} \cdots \overline{r}_0)_b
\]

Each of the n values in \(Z_{n-1}, Z_0, X_{n-1}, Y_{n-1}, M_{n-1}\) to \(M_0, \overline{r}_{n-1}, \overline{r}_0\) represents one base-b digit (a 32-bit word).

\[ 
Z_{n-1}, X_{n-1}, Y_{n-1}, M_{n-1} \text{ and } \overline{r}_{n-1} \text{ are the most significant bits of } Z, X, Y, M, \text{ while } \\
Z_0, X_0, Y_0, M_0 \text{ and } \overline{r}_0 \text{ are the least significant bits.}
\]

If we define

\[ R = b^n \]

then, we can calculate the additional arguments as follows:

\[ 
\overline{r} = R^2 \mod M \\
M' = (M'' \times M + 1) = R \times R^{-1} \quad (\text{Equation } 15.2) \\
M'' = M'' \mod b
\]

(Equation \(15.2\) is written in a form suitable for calculations using the extended binary GCD algorithm.)

**Body Text:**
Software can implement large-number modular exponentiations in the following order:

1. Write \(\frac{N}{32} - 1\) to RSA_MODEXP_MODE_REG.
2. Write \(X_i, Y_i, M_i\) and \(\overline{r}_i (i = [0,n] \cap N)\) to memory blocks RSA_X_MEM, RSA_Y_MEM, RSA_M_MEM and RSA_Z_MEM. The capacity of each memory block is 128 words. Each word of each memory block can store one base-b digit.
3. Write \(M'\) to RSA_M_PRIME_REG.
4. Write 1 to RSA_MODEXP_START_REG.
5. Wait for the operation to be completed. Poll RSA_INTERRUPT_REG until it reads 1, or until the RSA_INTEGRATE INTERRUPT is generated.

**Footer:**
Espressif Systems  
288  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)