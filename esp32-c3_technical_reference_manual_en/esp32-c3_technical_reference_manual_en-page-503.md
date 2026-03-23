

```markdown
Chapter 20 RSA Accelerator (RSA) GoBack

accelerator when Digital Signature (DS) is working.

## 20.3.1 Large Number Modular Exponentiation

Large-number modular exponentiation performs $Z = X^Y \bmod M$. The computation is based on Montgomery multiplication. Therefore, aside from the $X$, $Y$, and $M$ arguments, two additional ones are needed — $\overline{r}$ and $M'$, which need to be calculated in advance by software.

RSA Accelerator supports operands of length $N = 32 \times x$, where $x \in \{1, 2, 3, \dots, 96\}$. The bit lengths of arguments $Z$, $X$, $Y$, $M$, and $\overline{r}$ can be arbitrary $N$, but all numbers in a calculation must be of the same length. The bit length of $M'$ must be 32.

To represent the numbers used as operands, let us define a base-$b$ positional notation, as follows:

$$
b = 2^{32}
$$

Using this notation, each number is represented by a sequence of base-$b$ digits:

$$
n = \frac{N}{32}
$$

$$
Z = (Z_{n-1} Z_{n-2} \cdots Z_0)_b
$$

$$
X = (X_{n-1} X_{n-2} \cdots X_0)_b
$$

$$
Y = (Y_{n-1} Y_{n-2} \cdots Y_0)_b
$$

$$
M = (M_{n-1} M_{n-2} \cdots M_0)_b
$$

$$
\overline{r} = (\overline{r}_{n-1} \overline{r}_{n-2} \cdots \overline{r}_0)_b
$$

Each of the $n$ values in $Z_{n-1} \cdots Z_0$, $X_{n-1} \cdots X_0$, $Y_{n-1} \cdots Y_0$, $M_{n-1} \cdots M_0$, $\overline{r}_{n-1} \cdots \overline{r}_0$ represents one base-$b$ digit (a 32-bit word).

$Z_{n-1}$, $X_{n-1}$, $Y_{n-1}$, $M_{n-1}$ and $\overline{r}_{n-1}$ are the most significant bits of $Z$, $X$, $Y$, $M$, while $Z_0$, $X_0$, $Y_0$, $M_0$ and $\overline{r}_0$ are the least significant bits.

If we define $R = b^n$, the additional arguments can be calculated as $\overline{r} = R^2 \bmod M$.

The following equation in the form compatible with the extended binary GCD algorithm can be written as:

$$
M^{-1} \times M + 1 = R \times R^{-1}
$$

$$
M' = M^{-1} \bmod b
$$

Large-number modular exponentiation can be implemented as follows:

1. Write 1 or 0 to the RSA_INTERRUPT_ENA_REG register to enable or disable the interrupt function.

2. Configure relevant registers:
   (a) Write $(\frac{N}{32} - 1)$ to the RSA_MODE_REG register.
   (b) Write $M'$ to the RSA_M_PRIME_REG register.
```