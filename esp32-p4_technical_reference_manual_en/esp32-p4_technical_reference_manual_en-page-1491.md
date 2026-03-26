

```markdown
| Working Mode | Configuration Method                     |
|--------------|-------------------------------------------|
| Typical SHA  | Set SHA_START_REG to 1                    |
| DMA-SHA      | Set SHA_DMA_START_REG to 1                |

Table 29.3-2. SHA Hash Algorithm Selection

<table><thead><tr><td>Hash Algorithm</td><td>SHA_MODE_REG Configuration</td></tr></thead><tbody><tr><td>SHA-1</td><td>0</td></tr><tr><td>SHA-224</td><td>1</td></tr><tr><td>SHA-256</td><td>2</td></tr><tr><td>SHA-384</td><td>3</td></tr><tr><td>SHA-512</td><td>4</td></tr><tr><td>SHA-512/224</td><td>5</td></tr><tr><td>SHA-512/256</td><td>6</td></tr><tr><td>SHA-512/t</td><td>7</td></tr></tbody></table>

Notice:
ESP32-P4's RSA Digital Signature Peripheral (RSA_DS) and HMAC Accelerator (HMAC) modules also call the SHA accelerator when working. Therefore, users cannot access the SHA accelerator when these modules are working.
```

## 29.4 Function Description

The SHA accelerator generates the message digest via two steps: **Preprocessing** and **Hash operation**.

### 29.4.1 Preprocessing

Preprocessing consists of three steps: padding the message, parsing the message into message blocks and setting the initial hash value.
```