**Chapter Title:**
Chapter 20 RSA Accelerator (RSA)

**Section Heading and Subheading with Content:**

**20.3.3 Large Number Multiplication**

Large-number multiplication performs \( Z = X \times Y \). The length of result \( Z \) is twice that of operand \( X \) and operand \( Y \). Therefore, the RSA Accelerator only supports Large Number Multiplication with operand length \( N = 32 \times x \), where \( x \in {1, 2, 3, \ldots, 64} \). The length \( \hat{N} \) of result is \( Z = 2 \times N \).

The computation can be executed as follows:
1. Write 0 to the `RSA_INTERRUPT_ENA_REG` register to enable or disable the interrupt function.
2. Write \( (\frac{\hat{N}}{32} - 1), i.e., (\frac{\hat{N}}{16} - 1) \) to the `RSA_MODE_REG` register.
3. Write \( X_i \) and \( Y_i \) for \( i \in {0, 1, \ldots, n-1} \) to memory blocks `RSA_X_MEM` and `RSA_Z_MEM`. The capacity of each memory block is 64 words. Each word of each memory block can store one base-\( b \) digit. The memory blocks use the little-endian format for storage; i.e., the least significant digit of each number is in the lowest address.
   - \( n \) is calculated as:
     \[
     n = 32
     \]
4. Write \( X_i \) and \( Y_i \) to memory blocks `RSA_X_MEM` (for words from i=0,1,...n-1).
5. Note that the address of each word in these registers will not be written.
6. Users need to write data into any block only according to length; beyond this is ignored.

**20.3.4 Options for Acceleration**

The ESP32-S3 RSA accelerator also provides `SEARCH` and `CONSTANT_TIME` options that can accelerate the large-number modular exponentiation by default, both are configured no acceleration.
- Users may choose one or two of these to speed up computation:
  - To calculate \( Z = X^Y \) mod M when neither option is used. The time required depends on operand lengths.

**Footer:**
Espressif Systems
Page number and document version information (876 ESP32-S3 TRM [Version 1.7])