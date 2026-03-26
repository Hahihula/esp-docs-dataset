

```markdown
## 36.2 Terminology

### Image Interface

- **MIPI-CSI**: Camera serial interface, a high-speed serial interface for cameras compliant with MIPI specifications.
- **DVP**: Digital video parallel interface, generally composed of vsync, hsync, de, and data signals.
- **RAW**: Unprocessed data directly output from an image sensor, typically divided into R, Gr, Gb, and B channels. Classified into RAW8, RAW10, RAW12, etc., based on bit width.
- **RGB**: Colored image format composed of red, green, and blue colors. Classified into RGB888, RGB565, etc., based on the bit width of each color.
- **YUV**: Colored image format composed of luminance and chrominance. Classified into YUV444, YUV422, YUV420, etc., based on the data arrangement.

## 36.3 Feature List

ISP supports the following features:

- maximum resolution: 1920 x 1080
- three input channels: MIPI-CSI, DVP, and VDMA
- input formats: RAW8, RAW10, and RAW12
- output formats: RAW8, RGB888, RGB565, YUV422, and YUV420
- pipeline features:

  - Black level correction (BLC)
  - Defect pixel correction (DPC)
  - Bayer filter (BF)
  - Lens shading correction (LSC)
  - Demosaic
  - White balance gain (WBG)
  - Color correction matrix (CCM)
  - Gamma correction
  - RGB2YUV
  - Sharpen
  - Contrast/hue/saturation/luminance adjustment (COLOR)
  - YUV_limit
  - YUV2RGB
  - Crop
  - Automatic exposure statistics (AE)
  - Automatic focus statistics (AF)
```