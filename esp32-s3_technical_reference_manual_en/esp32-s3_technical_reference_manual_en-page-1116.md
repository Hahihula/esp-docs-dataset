**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Body Text with Code References and Descriptions:**

- **RX data**
  - When `SPI_USR_MISO_HIGHPART` is cleared, i.e., high part mode is disabled, RX data is saved to `SPI_WO_REG ~ SPI_W15_REG`, and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 64, the data in `SPI_WO_REG ~ SPI_W15_REG` may be overwritten.
    - For instance: 
      ```
      66 bytes (byte0 ~ byte65) are received, byte65 and byte64 will be stored to the addresses of (65 % 64 = 1), i.e., (64 % 64 = 0), i.e., `SPI_WO_REG[15:8]` and `SPI_WO_REG[7:0]`.
      ```
    - For this case, the content of `SPI_WO_REG[15:0]` may be overwritten.
  
  - When `SPI_USR_MISO_HIGHPART` is set, i.e., high part mode is enabled, the RX data is saved to `SPI_W8_REG ~ SPI_W15_REG`, and the data address is incremented by 1 on each byte transferred. If the data byte length is larger than 32, in `SPI_W8_REG ~ SPI_W15_REG` may be overwritten.
    - For instance:
      ```
      The content of `SPI_W8_REG[SPI_W15_REG]` can be stored to the addresses (64 % 32 = 0), i.e., byte31 and byte32 will be saved in `SPI_W8_REG[7:0]`.
      ```

**Note Section with Code References:**
- TX/RX data address mentioned above are both byte-addressable. Address 0 stands for `SPI_WO_REG[7:0]`, and Address 1 for `SPI_WO_REG[15:8]`, etc.
- The largest address is in `SPI_W15_REG[31:24]`.
- To avoid any possible error in TX/RX data, such as TX data being sent more than once or RX data being overwritten, please make sure the registers are configured correctly.

**Subsection Title and Description with Code References (Section 30.5.5.2):**
CPU-Controlled Slave Mode

- In a CPU-controlled slave full-duplex or half-duplex transfer, the RX data or TX data is saved to or sent from `SPI_WO_REG ~ SPI_W15_REG`, which are byte-addressable.
  
  - **In full-duplex communication:**
    ```
    The address of `SPI_WO_REG ~ SPI_W15_REG` starts from 0 and is incremented by 1 on each byte transferred. If the data address is larger than 63, the content of `SPI_W15_REG[31:24]` is overwritten.
    ```

  - **In half-duplex communication:** 
    ```
    The ADDR value in transmission format is the start address of the RX or TX data, corresponding to the registers `SPI_WO_REG ~ SPI_W15_REG`. The RX or TX address is incremented by 1 on each byte transferred. If the address is larger than 63 (the highest byte address), i.e., `SPI_W15_REG[31:24]`, the address of overflowing data is always 63 and only the content of `SPI_W15_REG[31:24]` is overwritten.
    ```

**Application Note with Code References for Usage (Section at bottom):**
- According to your applications, the registers `SPI_WO_REG ~ SPI_W15_REG` can be used as:
  - data buffers only
  - data buffers and status buffers

**Footer:**
Espressif Systems  
Page number: 1116  
Document version (Version 1.7)