

```markdown
## 28.4.2 Data and Data Block

ESP32-C5's ECDSA accelerator can operate on data of 192, 256, 384, or 512 bits. For example, the data (D[255:0]) can be divided into 32-bit data blocks.

Take 256-bit long data as an example, D[n][31:0] (n = 0, 1, ..., 7). Data blocks with the smaller serial number correspond to the lower binary bits. To be specific:

D[255:0] = D[7][31:0], D[6][31:0], D[5][31:0], D[4][31:0], D[3][31:0], D[2][31:0], D[1][31:0], D[0][31:0]

### 28.4.2.1 Writing Data

Writing data means writing data to an ECDSA memory block and using this data as the input to the ECDSA algorithm. To be specific, writing data to an ECDSA memory block means writing D[n][31:0] to the "starting address of this ECDSA memory block + 4 × n". For a 256-bit long data:

* write D[0] to "starting address"
* write D[1] to "starting address + 4"
* ...
* write D[7] to "starting address + 28"

**Note:**
When storing data, write only the data block of the required length. Do not append a 0 to the most significant bit. For example, for 192-bit data, store only the 192 bits without appending 0.

### 28.4.2.2 Reading Data

Reading data means reading data from the starting address of an ECDSA memory block and using this data as the output from the ECDSA algorithm. To be specific, reading data from an ECDSA memory block means reading D[n][31:0] from the "starting address of this ECDSA memory block + 4 × n". For a 256-bit long data:

* read D[0] from "starting address"
* read D[1] from "starting address + 4"
* ...
* read D[7] from "starting address + 28"

**Note:**
When reading data, only the data block of the required length needs to be read. For example, to read 192-bit data, simply read the lower 192 bits (i.e., 6 data blocks).

### 28.4.2.3 Padding the Message

The SHA accelerator can only process message blocks of 512 bits. Thus, all the messages should be padded to a multiple of 512 bits before the hash operation.

Suppose that the length of the message M is L_M bits. Then M shall be padded as introduced below:
```