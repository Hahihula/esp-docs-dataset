

```markdown
7.2.2 Architectural Overview 326
7.2.3 Features 326
7.2.4 Functional Description 327
    7.2.4.1 HP System Clock 327
    7.2.4.2 LP System Clock 328
    7.2.4.3 Peripheral Clocks 328
    7.2.4.4 PMU Control of High-Performance System Clock Gating 331
7.3 Programming Procedures 333
    7.3.1 HP System Clock Configuration 333
    7.3.2 LP System Clock Configuration 333
    7.3.3 Peripheral Clock Reset and Configuration 333
7.4 Register Summary 336
    7.4.1 PCR Register Summary 336
    7.4.2 LP System Clock Register Summary 338
7.5 Registers 339
    7.5.1 PCR Registers 339
    7.5.2 LP System Clock Registers 378

8 Chip Boot Control 386
8.1 Overview 386
8.2 Functional Description 386
    8.2.1 Default Configuration 387
    8.2.2 Boot Mode Control 387
    8.2.3 SDIO Sampling and Driving Clock Edge Control 389
    8.2.4 ROM Messages Printing Control 389
    8.2.5 JTAG Signal Source Control 390

9 Interrupt Matrix 391
9.1 Overview 391
9.2 Interrupt Terminology in ESP32-C61 391
    9.2.1 Interrupt 391
    9.2.2 Interrupt Signal/Interrupt Source 391
    9.2.3 Interrupt Flow in ESP32-C61 392
9.3 Features 392
9.4 Architecture 392
9.5 Functional Description 393
    9.5.1 Peripheral Interrupt Sources 393
    9.5.2 HP CPU Interrupts 396
    9.5.3 Assign Peripheral Interrupt Source to HP CPU Peripheral Interrupt 396
        9.5.3.1 Assign One Peripheral Interrupt Source to HP CPU Peripheral Interrupt 396
        9.5.3.2 Assign Multiple Peripheral Interrupt Sources to HP CPU Peripheral Interrupt 396
        9.5.3.3 Unassign SOURCE 396
    9.5.4 Delegated Interrupts 397
    9.5.5 Query Current Interrupt Status of SOURCE 397
9.6 Register Summary 398
    9.6.1 Interrupt Matrix Register Summary 398
```