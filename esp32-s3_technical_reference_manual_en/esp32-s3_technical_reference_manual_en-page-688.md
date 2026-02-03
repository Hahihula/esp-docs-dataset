Title: Chapter 15 Permission Control (PMS)

Body Text:
- The first split line to further split the data Region (DRAMo_split_line_0):
  - PMS_CORE_X_IRAM0_DRAMO_DMA_SPLIT_LINE CONSTRAIN_4 REGARD

- The second split line to further split the data Region (DRam0_split_line_1):
  - PMS_CORE_X_IRAM0_DRAMO_DMA_SPLIT_LINE CONSTRAIN_5 REGARD

Subtitle: When configuring the split lines,

Numbered List:
1. First configure the block in which the split line is by:

   - Configuring the Category_x field for the block in which the split line is to 0x1 or 0x2 (no difference)
   - Configuring the Category_0 ~ Category_x-1 fields for all the preceding blocks to 0x0
   - Configuring the Category_x+1 ~ Category_6 fields for all blocks afterwards to 0x3

For example, assuming you want to configure the split line in Block5, then first configure the Category_3 field for Block5 to 0x1 or 0x2; configure the Category_0 ~ Category_2 fields for Block2 ~ Block4 to 0x0; and configure the Category_4 ~ Category_6 fields for Block6 ~ Block8 to 0x3 (see illustration in Figure 15.3-2). On the other hand, when reading 0x1 or 0x2 from Category_3, then you know the split line is in Block5.

2. Configure the position of the split line inside of the configured block by:

   - Writing the [15:8] bits of the actual address at which you want to put the memory to the SPLITADDR field for the block in which the split line is.
   - Note that the split address must be aligned to 256 bytes, meaning you can only write the integral multiples of 0x100 to the SPLITADDR field.

For example, if you want to put the instruction region at 0x3fc88000, then write the [15:8] bits of this address, which is 0b10000000, to SPLITADDR.

Image Caption:
Figure 15.3-2. An illustration of Configuring the Category fields

Note section at bottom:

Subtitle: Note the following points when configuring the split lines:

Bulleted List:
- Position:

Hyperlink/Reference Texts in Image (not clickable):
- GoBack
- ESP32-S3 TRM (Version 1.7)

Footer Information:
- Espressif Systems
- Submit Documentation Feedback

Page Number: 
688