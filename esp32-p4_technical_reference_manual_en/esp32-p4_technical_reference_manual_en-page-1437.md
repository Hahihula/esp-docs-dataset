

```markdown
3. Hardware gets ready for CTR encryption by obtaining the result of applying Standard Incrementing Function INC₃₂ to J₀.
4. Hardware executes the GCTR Algorithm to encrypt the padded plaintext P, then executes the GHASH Algorithm to perform Hash computation on the padded ciphertext C.
5. Hardware executes the GHASH Algorithm to perform Hash computation on AAD Blocks, obtaining a 128-bit Hash result.
6. Hardware executes the GCTR Algorithm to encrypt J₀, obtaining T₀.
7. Software obtains the result T₀ from hardware, and executes MSBₜ Algorithm to obtain the final authentication tag T.

The only difference between GCM decryption and GCM encryption lies in Step 4 in Figure 25.7-1. To be more specific, instead of executing GCTR Algorithm to encrypt the padded plaintext, the AES Accelerator executes the same algorithm to decrypt the padded ciphertext in GCM decryption. For details, please see NIST SP 800-38D.

## 25.7.1 Hash Subkey

During GCM operation, the Hash subkey H is a 128-bit value computed by hardware, which is demonstrated in Step 1 in Figure 25.7-1. Also you can find more information about Hash subkey at “Step 1. Let H = CIPHₖ(0¹²⁸)” in Chapter 7 GCM Specification of NIST SP 800-38D.

The Hash subkey H is stored in the AES_H_MEM memory. Just like other endianness, its most significant (i.e., left-most) byte Byte0 is stored at the lowest address in the memory while least significant (i.e., right-most) byte Byte15 at the highest address. For details, see Table 25.5-2.

## 25.7.2 J₀

J₀ is a 128-bit value computed by hardware, which is required during Step 3 and Step 6 in Figure 25.7-1. For details on the generation of J₀, please see Chapter 7 GCM Specification in NIST SP 800-38D.

J₀ is stored in the AES_JO_MEM memory. Just like other endianness, its most significant (i.e., left-most) byte Byte0 is stored at the lowest address in the memory while least significant (i.e., right-most) byte Byte15 at the highest address. For details, see Table 25.5-2.

## 25.7.3 Authentication Tag

Authentication Tag (Tag for short) is one of the key results of GCM computation, which is demonstrated in Step 7 of Figure 25.7-1. The value of the Tag is determined by its length t (1 <= t <= 128):

* When t = 128, the value of Tag equals to T₀, a 128-bit string that is stored in the AES_TO_MEM. Just like other endianness, its most significant (i.e., left-most) byte Byte0 is stored at the lowest address in the memory while least significant (i.e., right-most) byte Byte15 at the highest address. For details, see Table 25.5-2.
* When 1 <= t < 128, the value of Tag equals to the t most significant (i.e., left-most) bits of T₀. In this case, Tag is represented as MSBₜ(T₀), which returns the t most significant bits of T₀. For example, MSB₄(111011010) = 1110 and MSB₅(11010011010) = 11010. For details on the MSBₜ() function, please refer to Chapter 6 Mathematical Components of GCM in NIST SP 800-38D.
```