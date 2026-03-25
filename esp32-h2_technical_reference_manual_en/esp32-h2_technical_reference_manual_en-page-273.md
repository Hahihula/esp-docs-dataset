

```markdown
registers of peripherals, see Section 7.4 Register Summary.

## 7.2 Clock

### 7.2.1 Overview

ESP32-H2 clocks are mainly sourced from oscillator (OSC), RC, and PLL circuits, and then processed by the dividers or selectors, which allows most functional modules to select their working clock according to their power consumption and performance requirements. Figure 7.2-1 shows the system clock structure.

### 7.2.2 Architectural Overview

![Figure 7.2-1. System Clock](image)

### 7.2.3 Features

ESP32-H2 clocks can be classified into two types depending on their frequencies:
```