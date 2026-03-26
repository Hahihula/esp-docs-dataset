

```markdown
Chapter 1 High-Performance CPU

1.11.2 Debug Halt Groups

1.11.2.1 Overview

In a multi-core system, when the debugging software is running on a given core, it is useful that other cores do not change the state of the system. This requirement is addressed by synchronous halt and resume. It is important that halt/resume information is communicated as quickly as possible to other cores. So, it is better to do it based on chip infrastructure rather than commands through the debugger software running on the host.

1.11.2.2 Features

* Support cross-triggering between HP cores
* Overriding the RunStall functionality of a core

1.11.2.3 Functional Description

HP core debug module implements dmcs2 register specified in the upcoming specification, RISC-V External Debug Version 1.0-STABLE, to implement simultaneous halting/resuming based on hart groups.
```