

```markdown
RTC FAST Memory | 0x5000_0000 | 0x5000_1FFF |
|---|---|

ESP32-C3's RTC FAST Memory can be further split into 2 regions. Each split region can be configured independently with different access.

The Register for configuring the split line is described below:

Table 14.4-9. Split RTC FAST Memory into the Higher Region and the Lower Region

| Split Lines Configuration Register¹ | Privileged Environment PIF_PMS_CONSTRAN_9_REG [10:0] | Unprivileged Environment PIF_PMS_CONSTRAN_9_REG [21:11] |
|---|---|---|
```