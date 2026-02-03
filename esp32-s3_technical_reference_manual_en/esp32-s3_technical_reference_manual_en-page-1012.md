Title: Chapter 27 I2C Controller (I2C)

Subtitle: GoBack

Section Title: 27.5.8.1 Introduction

Body Text:

Figure Caption:
- Figure 27.5-8, I2Cmaster Reading I2Cslave with a 7-bit Address in Segments

Diagram Descriptions and Annotations for the Diagrams (noting that these are block diagrams):

1. The first diagram shows an interaction between Master and Slave devices using SCL and SDA lines.
   - **Master Side:**
     - `cmd`
     - `op_code`
     - `byte_num`
   - Commands:
     - `cmd0` -> `RSTART`
     - `cmd1` -> `WRITE 1`
     - `cmd2` -> `READ N`
     - `cmd3` -> `END`
   - **Slave Side:**
     - RAM addresses (addr0 to addr(N-1)) with corresponding byte values.

2. The second diagram shows another interaction between Master and Slave devices using SCL and SDA lines.
   - Similar structure as the first, but it indicates a different segment handling mechanism:
     - `cmd`
     - `op_code`
     - `byte_num` (M-1)
   - Commands for Segment0 to Segment2 are shown with corresponding RAM addresses.

Body Text:

Figure 27.5-8 shows how I2Cmaster reads (N+M) bytes of data from an I2C slave in two/three segments separated by END commands. Configuration procedures are described as follows:
1. The procedures for Segment0 is similar to [27.5-5](#), except that the last command is an END.
2. Prepare data in the TX RAM of I2Cslave, and set I2CTrans_Start to start data transfer. After executing the END command, I2Cmaster refreshes command registers and the RAM as shown in Segment1, and clears the corresponding I2C_endDetect_INT interrupt. If cmd2 in Segment1 is a STOP, then data is read from I2Cslave in two segments. I2Cmaster resumes data transfer by setting I2C_trans_start and terminates the transfer by sending a STOP bit.
3. If cmd2 in Segment1 is an END, then data is read from I2Cslave in three segments.

Footer:
- Espresso Systems
- 1012 ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback

(Note: The text "[27.5-5](#)" indicates a reference to another section or figure, which is not provided here.)