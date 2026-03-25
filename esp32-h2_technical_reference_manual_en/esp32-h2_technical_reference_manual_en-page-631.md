

```markdown
## 22.3.1 Large-Number Modular Exponentiation

Large-number modular exponentiation performs $Z = X^Y \bmod M$. The computation is based on Montgomery multiplication. Therefore, aside from the $X$, $Y$, and $M$ arguments, two additional ones are needed — $\overline{r}$ and $M'$, which need to be calculated in advance by software.

The RSA accelerator supports operands of length $N = 32 \times x$, where $x \in \{1, 2, 3, \dots, 96\}$. The bit lengths of arguments $Z$, $X$, $Y$, $M$, and $\overline{r}$ can be arbitrary $N$, but all numbers in a calculation must be of the same length. The bit length of $M'$ must be 32.

To represent the numbers used as operands, let us define a base-$b$ positional notation, as follows:

$$
b = 2^{32}
$$

Using this notation, each number is represented by a sequence of base-$b$ digits:

$$
\frac{N}{32} \\
Z = (Z_{n-1}Z_{n-2}\cdots Z_0)_b \\
X = (X_{n-1}X_{n-2}\cdots X_0)_b \\
Y = (Y_{n-1}Y_{n-2}\cdots Y_0)_b \\
M = (M_{n-1}M_{n-2}\cdots M_0)_b \\
\overline{r} = (\overline{r}_{n-1}\overline{r}_{n-2}\cdots \overline{r}_0)_b
$$

Each of the values in $Z_{n-1}\cdots Z_0$, $X_{n-1}\cdots X_0$, $Y_{n-1}\cdots Y_0$, $M_{n-1}\cdots M_0$, $\overline{r}_{n-1}\cdots \overline{r}_0$ represents one base-$b$ digit (a 32-bit word).

$Z_{n-1}$, $X_{n-1}$, $Y_{n-1}$, $M_{n-1}$ and $\overline{r}_{n-1}$ are the most significant bits of $Z$, $X$, $Y$, $M$, while $Z_0$, $X_0$, $Y_0$, $M_0$ and $\overline{r}_0$ are the least significant bits.

If we define $R = b^n$, the additional argument $\overline{r}$ can be calculated as $\overline{r} = R^2 \bmod M$.

Also, argument $M'$ can be calculated using the formula below:

$$
M' = -M^{-1} \bmod b
$$

where, $M^{-1}$ is the **modular multiplicative inverse** of $M$, and it can be calculated with the extended binary GCD algorithm.

Large-number modular exponentiation on the ESP32-H2 can be implemented as follows:

1. Write 1 or 0 to the `RSA_INT_ENA` field to enable or disable the interrupt function.
2. Configure relevant registers:
    (a) Write $(\frac{N}{32} - 1)$ to the `RSA_MODE_REG` register.
    (b) Write $M'$ to the `RSA_M_PRIME_REG` register.
    (c) Configure registers related to the acceleration options, which are described later in Section 22.3.4.
3. Write $X_i$, $Y_i$, $M_i$ and $\overline{r}_i$ for $i \in \{0, 1, \dots, n-1\}$ to memory blocks `RSA_X_MEM`, `RSA_Y_MEM`, `RSA_M_MEM` and `RSA_Z_MEM`. The capacity of each memory block is 96 words. Each word of each memory block can store one base-$b$ digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address.
```