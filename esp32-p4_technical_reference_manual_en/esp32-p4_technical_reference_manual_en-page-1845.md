

```markdown
- length[13:0]/HB:
    - When 2DEN = 0, this field represents the length of the data being transferred (least significant 14 bits). For data reception, this field is filled in after the hardware receives a frame of data. For data transmission, this field indicates the length of the data to be sent. The unit is byte.
    - When 2DEN = 1, this field represents the horizontal width of the picture block (HB). The unit is pixel.

- size[13:0]/VB:
    - When 2DEN = 0, this field represents the size of the memory space allocated for transferring data (least significant 14 bits). The unit is byte.
    - When 2DEN = 1, this field represents the vertical height of the picture block (VB). The unit is pixel.

- length[28:14]/HA:
    - When 2DEN = 0, this field represents the length of the transferred data (most significant 14 bits, only bit14–bit27 is used). For data reception, this field is filled after the hardware receives a frame of data. For data transmission, this field indicates the length of the data to be sent. The unit is byte.
    - When 2DEN = 1, this field represents the horizontal width of the picture corresponding to the descriptor (HA). The unit is pixel.

- size[27:14]/VA:
    - When 2DEN = 0, this field represents the size of the memory space for transferring data (most significant 14 bits). The unit is byte.
    - When 2DEN = 1, this field represents the vertical height of the picture corresponding to the descriptor (VA). The unit is pixel.

- Buffer address pointer:
    - When 2DEN = 0, it is the buffer address pointer.
    - When 2DEN = 1, it is the address pointer of the origin coordinates of the HA × VA picture block in the buffer.

- Next descriptor address: Next descriptor address pointer.

39.5.2.3 Transfer Initialization

H264_DMA will read the linked list from the internal memory to the local according to the configuration of the registers related to each channel linked list descriptor, so that it can be used by the corresponding channel to transfer data, thereby start the corresponding channel.

The registers associated with each linked list descriptor are as follows:

- H264_DMA_OUTLINK/INLINK_START_CHx: This register controls whether the corresponding channel of H264_DMA starts to obtain descriptors. Setting this register to 1 means that the corresponding channel starts to obtain the descriptor. After obtaining the descriptor, the hardware automatically sets this register to 0, and then automatically obtain subsequent descriptors. x can be 0, 1, 2, 3, and 4, indicating the registers corresponding to channels 0, 1, 2, 3, and 4.

- H264_DMA_OUTLINK/INLINK_ADDR_CHx: This register represents the memory address where the first descriptor is stored, and the address requires 8-byte alignment.
```