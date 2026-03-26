

```markdown
Register 39.51. H264_SYS_STATUS_REG (0x00DC)
```

| Bit | Description |
|-----|-------------|
| 31-12 | (reserved) |
| 11   | H264_INTRA_FLAG |
| 10   | H264_DUAL_STREAM_SEL |
| 9    | H264_FRAME_NUM |

```markdown
H264_FRAME_NUM Represents the current frame number. (RO)

H264_DUAL_STREAM_SEL Represents which register group is used for the current frame.
- 0: Register group A is used
- 1: Register group B is used
(RO)

H264_INTRA_FLAG Represents the type of the current encoding frame.
- 0: P frame
- 1: I frame
(RO)
```

```markdown
Register 39.52. H264_FRAME_CODE_LENGTH_REG (0x00EO)
```

| Bit | Description |
|-----|-------------|
| 31-24 | (reserved) |
| 23   | H264_FRAME_CODE_LENGTH |

```markdown
H264_FRAME_CODE_LENGTH Represents the byte length of the current frame code. (RO)
```