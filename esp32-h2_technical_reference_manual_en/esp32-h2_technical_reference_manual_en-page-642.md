

```markdown
| Working Mode | Configuration Method |
|--------------|----------------------|
| Typical SHA | Set SHA_START_REG to 1 |
| DMA-SHA    | Set SHA_DMA_START_REG to 1 |

Users can choose hash algorithms by configuring the SHA_MODE_REG register. For details, please see Table 23.3-2.

Table 23.3-2. SHA Hash Algorithm Selection

<table><thead><tr><td>Hash Algorithm</td><td>SHA_MODE_REG Configuration</td></tr></thead><tbody><tr><td>SHA-1</td><td>0</td></tr><tr><td>SHA-224</td><td>1</td></tr><tr><td>SHA-256</td><td>2</td></tr></tbody></table>

Notice:
ESP32-H2's Digital Signature Algorithm (DSA) and HMAC Accelerator (HMAC) modules also call the SHA accelerator when working. Therefore, users cannot access the SHA accelerator when these modules are working.
```

## 23.4 Function Description

The SHA accelerator generates the message digest via two steps: Preprocessing and Hash operation.

### 23.4.1 Preprocessing

Preprocessing consists of three steps: padding the message, parsing the message into message blocks and setting the initial hash value.

#### 23.4.1.1 Padding the Message

The SHA accelerator can only process message blocks of 512 bits. Thus, all the messages should be padded to a multiple of 512 bits before the hash operation.

Suppose that the length of the message M is m bits. Then M shall be padded as introduced below:

1. First, append the bit "1" to the end of the message;
2. Second, append k bits of zeros, where k is the smallest, non-negative solution to the equation $m + 1 + k \equiv 448 \mod 512$;
3. Last, append the 64-bit block of value equal to the number m expressed using a binary representation.

For more details, please refer to FIPS PUB 180-4 Spec > Section "Padding the Message".

#### 23.4.1.2 Parsing the Message

The message and its padding must be parsed into N 512-bit blocks, $M^{(1)}, M^{(2)}, ..., M^{(N)}$. Since the 512 bits of the input block may be expressed as sixteen 32-bit words, the first 32 bits of message block i are denoted
```