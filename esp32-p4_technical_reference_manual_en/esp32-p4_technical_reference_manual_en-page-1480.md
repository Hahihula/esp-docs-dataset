

```markdown
also call the RSA accelerator when working. Therefore, users cannot access the RSA accelerator when the RSA Digital Signature Peripheral (RSA_DS) or the ECDSA Digital Signature Peripheral (ECDSA_DS) module is working.
```

## 28.3.1 Definitions and Representations

ESP32-P4's RSA accelerator supports operands of different lengths $N = 32 \times n$.

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
\bar{r} = (\bar{r}_{n-1} \bar{r}_{n-2} \cdots \bar{r}_0)_b
$$

Each of the values in $Z_{n-1} \cdots Z_0$, $X_{n-1} \cdots X_0$, $Y_{n-1} \cdots Y_0$, $M_{n-1} \cdots M_0$, $\bar{r}_{n-1} \cdots \bar{r}_0$ represents one base-$b$ digit (a 32-bit word).

$Z_{n-1}, X_{n-1}, Y_{n-1}, M_{n-1}$ and $\bar{r}_{n-1}$ are the most significant bits of $Z, X, Y, M$, while $Z_0, X_0, Y_0, M_0$ and $\bar{r}_0$ are the least significant bits.

If we define $R = b^n$, the additional argument $\bar{r}$ can be calculated as $\bar{r} = R^2 \bmod M$.

Also, argument $M'$ can be calculated using the formula below:

$$
M' = -M^{-1} \bmod b
$$

where, $M^{-1}$ is the **modular multiplicative inverse** of $M$, and it can be calculated with the extended binary GCD algorithm.

## 28.3.2 Large-Number Modular Exponentiation

Large-number modular exponentiation performs $Z = X^Y \bmod M$. The computation is based on Montgomery multiplication. Therefore, aside from the $X, Y$, and $M$ arguments, two additional ones are needed — $\bar{r}$ and $M'$, which need to be calculated in advance by software.

The RSA accelerator supports operands of length $N = 32 \times n$, where $n \in \{1, 2, 3, \dots, 128\}$. The bit lengths of arguments $Z, X, Y, M$, and $\bar{r}$ can be arbitrary $N$, but all numbers in a calculation must be of the same length. The bit length of $M'$ must be 32.

Large-number modular exponentiation on the ESP32-P4 can be implemented as follows:

1. Write 1 or 0 to the **RSA_INT_ENA** field to enable or disable the interrupt function.
2. Configure relevant registers:
   (a) Write $(\frac{N}{32} - 1)$ to the **RSA_MODE_REG** register.
```