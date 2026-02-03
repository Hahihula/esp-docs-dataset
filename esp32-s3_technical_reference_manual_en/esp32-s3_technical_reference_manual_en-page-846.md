**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Body Text:**

SHA-512/t for a given value of t can be calculated by performing SHA-512 from hexadecimal representation of the string “SHA-512/t”. It’s not hard to observe that when determining the initial hash values for SHA-512/t algorithms with different t, the only difference lies in the value of t.

Therefore, we have specially developed the following simplified method to calculate the initial hash value for SHA-512/t:

**Step 1: Generate t_string and t_length**
t_string is a 32-bit data that stores the input message of t. t_length is a 7-bit data that stores the length of the input message. The t_string and t_length are generated in methods described below, depending on the value of t:

- If \(1 \leq t < 9\), then \(t_{length} = 7'h48\) and \(t_string\) is padded in the following format:
\[ 
\begin{array}{c}
8'h30 + 8'h10 \\
1'b1 \\
23'b0
\end{array}
\]

where \( t_0 = t \).

For example, if \( t = 8 \), then \(t_{length} = 7'h48\) and \(t_string\) is padded in the following format:
\[ 
\begin{array}{c}
8'h30 + 8'h1 \\
1'b1 \\
15'b0
\end{array}
\]

where, \( t_0 = t \% 10 \) and \( t_{1} = t / 10 \).

For example, if \( t = 56 \), then \(t_{0} = 6\), \(t_{1} = 5\) ,and \(t_string = 32'h35368000\).

If \( 100 \leq t < 512 \), the \(t_{length} = 7'h58\) and \(t_string\) is padded in the following format:
\[ 
\begin{array}{c}
8'h30 + 8'h2 \\
1'b1 \\
7'b0
\end{array}
\]

where, \( t_0 = t \% 10 \), \( t_{1} = (t / 10) \% 10\) ,and \( t_{2} = t / 100 \).

For example, if \( t = 231 \), then \( t_{0} = 1\), \( t_{1} = 3\), and \( t_string = 32'h32333180\).

**Step 2: Initialize relevant registers**
Initialize SHA_T_STRING_REG and SHA_T_LENGTH_REG with the generated t_string and t_length in the previous step.

**Step 3: Obtain initial hash value**
Set the SHA_MODE_REG register to Set. The SHA_START_REG register to 1 to start the SHA accelerator. Then poll register SHA BUSY_REG until the content of this register becomes 0, indicating the calculation of initial hash value is completed.

Please note that the initial value for SHA-512/t can be also calculated according to Section “5.3.6 SHA-512/t” in FIPS PUB 180-4 Spec, which describes performing SHA-512 operation (with its initial hash value set to the result of 8-bitwise XOR operation of C and 0xa5) from the hexadecimal representation of the string “SHA-512/t”.

**Subsection Title:**
18.4.2 Hash Task Process

**Body Text for Subsection:**

After the preprocessing, the ESP32-S3 SHA accelerator starts to hash a message M and generates message digest of different lengths, depending on different hash algorithms. As described above, the ESP32-S3 SHA accelerator supports two working modes, which are Typical SHA and DMA-SHA. The operation process for the SHA accelerator under two working modes is described in the following subsections.

**Footer:**
Espressif Systems  
846  
ESP32-S3 TRM (Version 1.7)  

**Link Text at Bottom of Page:** 
Submit Documentation Feedback