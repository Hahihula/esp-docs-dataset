

```markdown
Chapter 22 AES Accelerator (AES) GoBack


Register 22.4. AES_MODE_REG (0x0040)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
|     | AES_MODE    |

<table>
<tr>
<td>Bit</td>
<td>Name</td>
<td>Description</td>
<td>Reset</td>
</tr>
<tr>
<td>7-6</td>
<td>AES_MODE</td>
<td>Configures the key length and encryption/decryption of the AES accelerator.</td>
<td></td>
</tr>
<tr>
<td>0</td>
<td>O: AES-128 encryption</td>
<td></td>
<td></td>
</tr>
<tr>
<td>1</td>
<td>Reserved</td>
<td></td>
<td></td>
</tr>
<tr>
<td>2</td>
<td>AES-256 encryption</td>
<td></td>
<td></td>
</tr>
<tr>
<td>3</td>
<td>Reserved</td>
<td></td>
<td></td>
</tr>
<tr>
<td>4</td>
<td>AES-128 decryption</td>
<td></td>
<td></td>
</tr>
<tr>
<td>5</td>
<td>Reserved</td>
<td></td>
<td></td>
</tr>
<tr>
<td>6</td>
<td>AES-256 decryption</td>
<td></td>
<td></td>
</tr>
<tr>
<td>7</td>
<td>Reserved</td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>(R/W)</td>
<td></td>
<td></td>
</tr>
</table>

Register 22.5. AES_TRIGGER_REG (0x0048)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
|     | AES_TRIGGER |

<table>
<tr>
<td>Bit</td>
<td>Name</td>
<td>Description</td>
<td>Reset</td>
</tr>
<tr>
<td>7-0</td>
<td>AES_TRIGGER</td>
<td>Configures whether to start AES operation.</td>
<td></td>
</tr>
<tr>
<td>1</td>
<td>O: No effect</td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>1: Start (WT)</td>
<td></td>
<td></td>
</tr>
</table>

Register 22.6. AES_DMA_ENABLE_REG (0x0090)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
|     | AES_DMA_ENABLE |

<table>
<tr>
<td>Bit</td>
<td>Name</td>
<td>Description</td>
<td>Reset</td>
</tr>
<tr>
<td>7-0</td>
<td>AES_DMA_ENABLE</td>
<td>Configures the working mode of the AES accelerator.</td>
<td></td>
</tr>
<tr>
<td>0</td>
<td>O: Typical AES</td>
<td></td>
<td></td>
</tr>
<tr>
<td>1</td>
<td>DMA-AES</td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>(R/W)</td>
<td></td>
<td></td>
</tr>
</table>

Espressif Systems
875
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```