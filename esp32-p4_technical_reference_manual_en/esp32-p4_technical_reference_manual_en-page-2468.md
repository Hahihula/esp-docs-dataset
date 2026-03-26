

```markdown
46.10.2.5 A-law/μ-law Compression and Decompression

ESP32-P4 I2Sn compresses/decompresses the storage data in 32-bit by A-law or by μ-law. By default, zeros are filled into high bits.

Configure I2S_RX_PCM_BYPASS:
- 0: Compress or decompress the data
- 1: Do not compress or decompress the data

Configure I2S_RX_PCM_CONF:
- 0: Decompress the data using A-law
- 1: Compress the data using A-law
- 2: Decompress the data using μ-law
- 3: Compress the data using μ-law

At this point, the data format control is completed. Data then is stored into memory via GDMA.

46.11 Event Task Matrix Feature

ESP32-P4 I2Sn supports the Event Task Matrix (ETM) function, which allows I2Sn’s ETM tasks to be triggered by any peripherals’ ETM events, or I2Sn’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to I2Sn. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

I2Sn can receive the following ETM tasks:
- I2Sn_TASK_START_TX: Enables I2Sn TX for data transfer.
- I2Sn_TASK_START_RX: Enables I2Sn RX for data transfer.
- I2Sn_TASK_STOP_TX: Stops I2Sn TX data transfer.
- I2Sn_TASK_STOP_RX: Stops I2Sn RX data transfer.

I2Sn can generate the following ETM events:
- I2Sn_EVT_TX_DONE: Indicates that I2Sn TX has completed data transmission.
- I2Sn_EVT_RX_DONE: Indicates that I2Sn RX has completed data reception.
- I2Sn_EVT_X_WORDS_SENT: Indicates that the word number sent by I2Sn TX is equal to or larger than the value set by I2S_ETM_TX_SEND_WORD_NUM.
- I2Sn_EVT_X_WORDS_RECEIVED: Indicates that the word number received by I2Sn RX is equal to or larger than the value set by I2S_ETM_RX_RECEIVE_WORD_NUM.

In practical applications, I2Sn’s ETM events can trigger its own ETM tasks. For example, the I2Sn_EVT_X_WORDS_SENT event can trigger the I2Sn_TASK_STOP_TX task, and in this way stop the I2Sn operation through ETM.
```