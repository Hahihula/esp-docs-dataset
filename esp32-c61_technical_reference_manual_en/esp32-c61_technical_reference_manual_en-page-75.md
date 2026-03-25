

```markdown
Chapter 1 ESP-RISC-V CPU

GoBack

1.6.4 Bit Manipulation (Zb) Extension

1.6.4.1 Overview

The bit-manipulation (bitmanip) extension, also known as the Zb extension set, consists of several component extensions to the base RISC-V architecture. These extensions aim to improve code density, performance, and energy efficiency. The HP core fully supports the Zb extension. For Zb extension specifications, please refer to Zb-specification v1.0.0.

1.6.4.2 Functional Description

Although the bitmanip instructions are designed for general-purpose use, certain instructions are more applicable to specific domains. Hence, the bitmanip extension set is divided into several smaller extensions instead of a single large one. Each extension has its own Zb*-extension name, and comprises instructions that share related functionality, use cases, and often the same implementation logic. Some instructions are available in only one extension, while others are available in several. The instructions have mnemonics and encodings that are independent of the extensions in which they appear. Thus, when implementing extensions with overlapping instructions, there is no redundancy in logic or encoding.
```