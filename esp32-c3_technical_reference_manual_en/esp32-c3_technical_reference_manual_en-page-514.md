

```markdown
DMA-SHA          Set SHA_DMA_START_REG to 1

Users can choose hash algorithms by configuring the SHA_MODE_REG register. For details, please see Table 21.3-2.

Table 21.3-2. SHA Hash Algorithm Selection

| Hash Algorithm | SHA_MODE_REG Configuration |
|----------------|------------------------------|
| SHA-1          | 0                            |
| SHA-224        | 1                            |
| SHA-256        | 2                            |

Notice:
ESP32-C3's Digital Signature (DS) and HMAC Accelerator (HMAC) modules also call the SHA accelerator. Therefore, users cannot access the SHA accelerator when these modules are working.

## 21.4 Function Description

SHA accelerator can generate the message digest via two steps: Preprocessing and Hash operation.

### 21.4.1 Preprocessing

Preprocessing consists of three steps: padding the message, parsing the message into message blocks and setting the initial hash value.

#### 21.4.1.1 Padding the Message

The SHA accelerator can only process message blocks of 512 bits. Thus, all the messages should be padded to a multiple of 512 bits before the hash task.

Suppose that the length of the message M is m bits. Then M shall be padded as introduced below:

1. First, append the bit "1" to the end of the message;
2. Second, append k bits of zeros, where k is the smallest, non-negative solution to the equation m + 1 + k ≡ 448 mod 512;
3. Last, append the 64-bit block of value equal to the number m expressed using a binary representation.

For more details, please refer to Section "5.1 Padding the Message" in FIPS PUB 180-4 Spec.

#### 21.4.1.2 Parsing the Message

The message and its padding must be parsed into N 512-bit blocks, M^(1), M^(2), ..., M^(N). Since the 512 bits of the input block may be expressed as sixteen 32-bit words, the first 32 bits of message block i are denoted M_0^(i), the next 32 bits are M_1^(i), and so on up to M_15^(i).

During the task, all the message blocks are written into the SHA_M_n_REG: M_0^(i) is stored in SHA_M_O_REG, M_1^(i) stored in SHA_M_1_REG, ..., and M_15^(i) stored in SHA_M_15_REG.
```