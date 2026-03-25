

```markdown
Figure 24.6-1. HMAC SHA-256 Padding Diagram

padding must be manually applied by the user. After the user prepared the padding data, they should complete the subsequent configuration according to the Section 24.5.

24.6.2 HMAC Algorithm Structure

The structure of the implemented algorithm in the HMAC module is shown in Figure 24.6-2. This is the standard HMAC algorithm as described in RFC 2104.

Figure 24.6-2. HMAC Structure Schematic Diagram

In Figure 24.6-2:

1. ipad is a 512-bit message block composed of 64 bytes of 0x36.
2. opad is a 512-bit message block composed of 64 bytes of 0x5c.

The HMAC module appends a 256-bit 0 sequence after the bit sequence of the 256-bit key K in order to get a 512-bit K₀. Then, the HMAC module XORs K₀ with ipad to get the 512-bit S1. Afterwards, the HMAC module appends the input message (multiple of 512 bits) after the 512-bit S1, and exercises the SHA-256 algorithm to get the 256-bit H1.

The HMAC module appends the 256-bit SHA-256 hash result H1 to the 512-bit S2 value, which is calculated using the XOR operation of K₀ and opad. A 768-bit sequence will be generated. Then, the HMAC module uses the SHA padding algorithm described in Section 24.6.1 to pad the 768-bit sequence to a 1024-bit sequence, and applies the SHA-256 algorithm to get the final hash result (256-bit).
```