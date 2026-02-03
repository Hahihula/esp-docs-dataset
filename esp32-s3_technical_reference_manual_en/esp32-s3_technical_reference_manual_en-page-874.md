**Title: Chapter 20 RSA Accelerator (RSA)**

**Subtitle: GoBack**

---

### **20.3.1 Large Number Modular Exponentiation**

Large-number modular exponentiation performs \( Z = X^Y \mod M \). The computation is based on Montgomery multiplication. Therefore, aside from the \(X\), \(Y\), and \(M\) arguments, two additional ones are needed — \(\tau\) and \(M'\), which need to be calculated in advance by software.

RSA Accelerator supports operands of length \(N = 32 \times x\), where \(x \in {1, 2, 3, \ldots, 128}\). The bit lengths of arguments \(Z\), \(X\), \(Y\), \(M\), and \(\tau\) can be arbitrary \(N\), but all numbers in a calculation must be of the same length. The bit length of \(M'\) must be at least twice that.

To represent the numbers used as operands, let us define a base-\(b\) positional notation, as follows:

\[ b = 2^{32} \]

Using this notation, each number is represented by a sequence of base-\(b\) digits:
\[ n = \frac{N}{32} \]
\[ Z = (Z_{n-1} \cdots Z_0)_{b} \]
\[ X = (X_{n-1} \cdots X_0)_{b} \]
\[ Y = (Y_{n-1} \cdots Y_0)_{b} \]
\[ M = (M_{n-1} \cdots M_0)_{b} \]
\[ r = (\tau_{n-1} \cdots \tau_0)_{b} \]

Each of the \(n\) values in \(Z_{n-1} \cdots Z_0, X_{n-1} \cdots X_0, Y_{n-1} \cdots Y_0, M_{n-1} \cdots M_0, r_{n-1} \cdots r_0\) represents one base-\(b\) digit (a 32-bit word).

\(Z_{n-1}, X_{n-1}, Y_{n-1}, M_{n-1}\) and \(r_{n-1}\) are the most significant bits of \(Z\), \(X\), \(Y\), \(M\), while \(\tau_0\) is one base-\(b\) digit (a 32-bit word).

\(Z_{n-1}, X_{n-1}, Y_{n-1}, M_{n-1}\) and \(r_{n-1}\) are the least significant bits.

If we define \(R = b^n\), then additional arguments can be calculated as \(\tau = R^2\) mod \(M\).

The following equation in the form compatible with the extended binary GCD algorithm can be written as:

\[ M^{-1} \times M + 1 = R \times R^{-1} \]

\[ M' = M^{-1} \mod b \]

Large-number modular exponentiation can be implemented as follows:
1. Write \(1\) or \(0\) to the `RSA_INTERRUPT_ENA_REG` register to enable or disable the interrupt function.
2. Configure relevant registers:

   (a) Write \(\frac{N}{32} - 1\) to the `RSA_MODE_REG` register.

   (b) Write \(M'\) to the `RSA_M_PRIME_REG` register.

   (c) Configure registers related to acceleration options, which are described later in Section **20.3.4**.

---

Espressif Systems  
874  
ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback