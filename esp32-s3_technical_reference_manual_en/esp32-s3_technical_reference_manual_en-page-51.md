**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Title and Reference Information:**
- Table Name: Extended Instruction List

**Column Headers in the Table:**
- Instruction Type
- Instruction^1
- Reference Section

**Content of the Table:**

1. **Read instructions**
   - LD.QR
   - EE.VLD.[8/64].[XP/IP]
   - EE.VLDBC.[8/16/32].[-/XP/IP]
   - EE.VLDHBC.16.INCP
   - EE.LDF.[64/128].[XP/IP]
   - EE.LD.128.USAR.[XP/IP]
   - EE.LDQ.A.[U/S][8/16/128].[XP/IP]
   - EE.LD.QACC_[H/L].[H/32/128].[IP]
   - EE.LD.ACCX.IP
   - EE.LD.UA STATE.IP

2. **Write instructions**
   - EE.LDXQ.32
   - ST.QR
   - EE.VST.[8/64].[XP/IP]
   - EE.VST.H.[L/64].[XP/IP]
   - EE.STF.[64/128].[XP/IP]
   - EE.ST.QACC_[H/L].[H/32/128].[IP]
   - EE.ST.ACCX.IP
   - EE.ST.UA.STATE.IP

3. **Data exchange instructions**
   - MV.QR
   - EE.MOV.I.32.A
   - EE.MOV.I.32.Q
   - EE.VZIP.[8/16/32]
   - EE.VUNZIP.[8/16/32]
   - EE.ZERO.Q
   - EE.ZERO.QACC
   - EE.ZERO.ACCX
   - EE.MOV.S8.QACC
   - EE.MOV.S16.QACC
   - EE.MOV.U8.QACC
   - EE.MOV.U16.QACC

4. **Arithmetic instructions**
   - EE.VADDS.[S/8/16/32].[-/LD.INCP/ST.INCP]
   - EE.VSUBS.S.[8/16/32].[-/LD.INCP/ST.INCP]
   - EE.VMLULS.U/S][8/16].[QACC.[-/LD.IP/LD.XP
   - EE.CMULS.[U/S][8/16].[QACC.[-/LD.IP/LD.XP
   - EE.VMULAS.U/S][8/16].[QACC.[-/LD.IP/LD.XP
   - EE.VMLULAS.U/S][8/16].[QACC.[-/LD.IP/LD.XP
   - EE.VSMULS.S.[8/16].[QACC.[-/LD.INCP

**Footer Information:**
- Page Number and Document Version:
  - "51 ESP32-S3 TRM (Version 1.7)"
  
- Company Name at the bottom of each page section:
  - Espressif Systems
  
- Feedback Link:
  - Submit Documentation Feedback