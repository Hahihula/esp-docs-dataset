**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Subtitle:**
26.3.5.2 Receiving Packets from SDIO Host

**Body Text:**
Transmission of packets from Host to Slave is initiated by the Host. The Slave receives data via DMA and stores it in RAM. After transmission is completed, the CPU will be interrupted to process the data. The whole procedure is demonstrated in Figure 26.3-7.

The diagram shows a flowchart with arrows indicating steps between "Host" and "Slave". Key points include:
- Host obtains available receiving buffers from Slave by accessing register SLCOHOST_TOKEN_RDATA.
- CPU should update this value after the receiving DMA linked list preparation is done (indicated as "发送CMD53").
- The process involves SDIO Physical Bus data transfer, with steps like "获取Slave可用的接收Buffer数" and "将Slave有足够的接收Buffer".
- There's a step for "填充数据包" which leads to "发送CMD53".

**Figure Caption:**
Figure 26.3-7. Packet Receiving Procedure (Initiated by Host)

**Additional Text Below Diagram:**
The process continues with:
- The Host obtains the number of available receiving buffers from the Slave by accessing register SLCOHOST_TOKEN_RDATA.
- The Slave CPU should update this value after the receiving DMA linked list is prepared.

HOSTREG_SLCO_TOKEN1 in SLCOHOST_TOKEN_RDATA stores the accumulated number of available buffers. 

The Host can figure out the available buffer space, using HOSTREG_SLCO_TOKEN1 minus the number of buffers already used.

If the buffers are not enough, the Host needs to constantly poll the register until there are enough buffers available.
To ensure sufficient receiving buffers, the Slave CPU must constantly load buffers on the receiving linked list. The process is shown in Figure 26.3-8 (referenced but image missing).

**Footer:**
Espressif Systems
568

**Link Texts:**
Submit Documentation Feedback
ESP32 TRM (Version 5.6)