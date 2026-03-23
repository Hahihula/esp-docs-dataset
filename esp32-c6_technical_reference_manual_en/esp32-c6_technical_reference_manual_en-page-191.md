

```markdown
Chapter 6 eFuse Controller    GoBack

6.3.6 Interrupts

• PGM_DONE interrupt: Triggered when eFuse programming has finished. To enable this interrupt, set the EFUSE_PGM_DONE_INT_ENA field of register EFUSE_INT_ENA_REG to 1.
• READ_DONE interrupt: Triggered when eFuse reading has finished. To enable this interrupt, set the EFUSE_READ_DONE_INT_ENA field of register EFUSE_INT_ENA_REG to 1.

Espressif Systems    191    ESP32-C6 TRM (Version 1.1)    Submit Documentation Feedback
```