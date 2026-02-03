Title: Chapter 21 HMAC Accelerator (HMAC)

Body Text:
- Append k bits of value "0", where k is the smallest non-negative number which satisfies m + 1 + k ≡ 448(mod512);
- Append a 64-bit integer value as a binary block. This block includes the length of the unpadded message as a big-endian binary integer value m.

Figure Caption:
- Figure 21.3-1. HMAC SHA-256 Padding Diagram

Body Text (continued):
In downstream mode, there is no need to input any message or apply padding. In upstream mode, if the length of the unpadded message is a multiple of 512 bits, the user can choose to configure hardware to apply the SHA padding. If the length is not a multiple of 512 bits, the user must apply the SHA padding manually. For detailed steps, please see Section 21.2.6.

Subtitle: 21.3.2 HMAC Algorithm Structure

Body Text (continued):
The structure of the implemented algorithm in the HMAC module is shown in Figure 21.3-2. This is the standard HMAC algorithm as described in RFC 2104.

Figure Caption:
- Figure 21.3-2. HMAC Structure Schematic Diagram

Footer: Espressif Systems, ESP32-S3 TRM (Version 1.7), Submit Documentation Feedback