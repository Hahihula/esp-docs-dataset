

# 1.13 Debug Cross-Triggering

## 1.13.1 Overview

In a multi-core system, when the debugging software is running on a given core, it is useful that the other cores do not change the state of the system. This requirement is addressed by synchronous halt and resume. It is important that halt/resume information is communicated as quickly as possible to other cores. So, it is better to do it based on chip infrastructure rather than commands through the debugger software running on the host.

## 1.13.2 Features

* Control register to enable or disable cross-trigger between cores
* Overriding the RunStall functionality of a core

## 1.13.3 Functional Description

Such a scheme has been implemented by providing a custom control register in the debug module. The register CORE_XT_EN implements a control bit to enable or disable cross-triggering mode. Once enabled, any core halted due to events such as hardware trigger and ebreak instructions will also result in halting of other cores without any intervention from the debugger. After halting of cores due to cross-trigger mode, it is not possible to resume without debugger intervention. The debugger has to connect to all cores and resume each core synchronously. Please note, debug cross trigger also halts any core which is stalled due to RunStall functionality.