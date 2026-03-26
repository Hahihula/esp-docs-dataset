

```markdown
Chapter 37 Pixel-Processing Accelerator (PPA)  
GoBack  

Register 37.8. PPA_BLEND_TRANS_MODE_REG (0x0034)  

(reserved)  
31  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  Reset  
5   PPA_BLEND_RST  PPA_BLEND_TRANS_MODE_UPDATE  PPA_BLEND_FIX_PIXEL_FILL_EN  PPA_BLEND_BYPASS  PPA_BLEND_EN  

PPA_BLEND_EN Configures whether to enable BLEND.  
O: Disable  
1: Enable  
(R/W)  

PPA_BLEND_BYPASS Configures whether to bypass BLEND and directly output the background layer.  
O: Bypass  
1: Not bypass  
(R/W)  

PPA_BLEND_FIX_PIXEL_FILL_EN Configures whether to enable filled image output.  
O: Disable  
1: Enable, where only BLEND TX works and the output pixel and size are configured by PPA_BLEND_TX_SIZE_REG and PPA_BLEND_TX_FIX_PIXEL.  
(R/W)  

PPA_BLEND_TRANS_MODE_UPDATE Write 1 to update the transfer mode, active PPA_BLEND_FIX_PIXEL_FILL_EN, and start BLEND workflow. (WT)  

PPA_BLEND_RST Configures whether to reset BLEND.  
O: Release reset  
1: Reset  
(R/W)
```