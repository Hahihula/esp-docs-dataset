

```markdown
36.5.2.7 Color Correction Matrix (CCM)

CCM is a correction matrix for image pixels that can adjust RGB888 pixels, including white balance adjustments. The relationship between the output R', G', B' and the input R, G, B is described by the following matrix. The parameters RR, RG, RB, GR, GG, GB, BR, BG, and BB can be configured with `ISP_CCM_xx`. Each parameter is a 13-bit fixed-point number, where bit [12] is the sign bit, bits [11:0] represent the absolute value of the number, bits [11:8] the integer part, and bits [7:0] the fractional part.

$$
\begin{bmatrix}
R' \\
G' \\
B'
\end{bmatrix}
=
\begin{bmatrix}
RR & RG & RB \\
GR & GG & GB \\
BR & BG & BB
\end{bmatrix}
\times
\begin{bmatrix}
R \\
G \\
B
\end{bmatrix}
\quad (36.1)
$$

36.5.2.8 Gamma Correction

This module is used to adjust the gamma curve of an image. The gamma curve should be configured before gamma correction is enabled. Gamma curves can be configured using registers, with each R, G, B channel having an independent curve consisting of 16 sampling points. For the X component (input value), the values are indirectly obtained through `ISP_GAMMA_R/G/B_Xn` (where n ranges from 00 to OF). The Y component (output value) can be directly set using `ISP_GAMMA_R/G/B_Yn` (where n ranges from 00 to OF). Once configuration is complete, writing 1 to `ISP_GAMMA_UPDATE` applies the gamma curve settings. The gamma curve is illustrated in Figure 36.5-1.

For the X component, taking the R channel as an example,

```
ISP_GAMMA_R_X(n) = log2(X(n) - X(n-1))
```

This means the nth X coordinate value is obtained by adding 2 to the power of `ISP_GAMMA_R_X(n)` to the (n-1)th X coordinate value. Specifically, for the last coordinate, `X(0F) = 2^ISP_GAMMA_R_X0F + X(0E) - 1`. Since RGB888 in ISP uses 8-bit integers, only the configuration where `X(0F) = 255` is considered a valid configuration.
```