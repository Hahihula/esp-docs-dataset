

```markdown
Chapter 41 Voice Activity Detection (VAD)
GoBack

## 41.6 Programming Procedure

### 41.6.1 Automatic Operation Mode

1. Configure the VAD parameters as described in Section 41.4.1.
2. Enable the VAD automatic detection mode by writing 1 to `LP_I2S_VAD_EN`.
3. Configure the LP I2S to operate in 16-bit receive mode and start receiving data in 16-bit format. The received data will be stored in the LP I2S memory.
4. The VAD module will automatically perform operations on each frame of data after the LP I2S receives the complete frame.
5. (Optional) When the VAD module triggers a wake-up source/interrupt signal, the LP I2S memory already contains the voice frame that triggered the VAD wake-up, along with the previous three voice frames. Users can read these four frames of voice data from the LP I2S memory via the LP core for subsequent processing. For details on the size of the LP I2S memory and data reading methods, please refer to Chapter 47 LP I2S Controller > Section 47.8.3 Internal Memory.

### 41.6.2 Manual Operation Mode

1. Configure the VAD parameters as described in Section 41.4.1.
2. Manually store the voice data in the LP I2S memory. For details, refer to Chapter 47 LP I2S Controller > Section 47.8.3 Internal Memory.
3. With all the voice data stored in the memory, write 1 to `LP_I2S_VAD_FORCE_START`, then the VAD will perform operations on one frame of data.
4. When the VAD module completes processing one frame of data, `LP_I2S_VAD_DONE_INT` interrupt will be generated.
```