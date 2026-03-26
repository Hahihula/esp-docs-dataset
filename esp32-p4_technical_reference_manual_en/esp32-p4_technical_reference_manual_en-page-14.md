
```markdown
10.2.2 Architectural Overview 638
10.2.3 Features 638
10.2.4 Functional Description 639
    10.2.4.1 HP System Clock 639
    10.2.4.2 LP System Clock 640
    10.2.4.3 Peripheral Clocks 641
10.3 Programming Procedures 645
    10.3.1 HP System Clock Configuration 645
    10.3.2 LP System Clock Configuration 646
    10.3.3 Peripheral Clock Reset and Configuration 646
10.4 Register Summary 648
    10.4.1 Reset and Clock (HP_SYS_CLKRST) Register Summary 648
    10.4.2 LP Always on Clock and Reset (LP_CLKRST) Register Summary 650
    10.4.3 LP Peripheral Clock and Reset (LPPERI) Register Summary 650
10.5 Registers 652
    10.5.1 Reset and Clock (HP_SYS_CLKRST) Registers 652
    10.5.2 LP Always on Clock and Reset (LP_CLKRST) Registers 742
    10.5.3 LP Peripheral Clock and Reset (LPPERI) Registers 762

11 Chip Boot Control 772
11.1 Overview 772
11.2 Functional Description 772
    11.2.1 Default Configuration 772
    11.2.2 Boot Mode Control 773
    11.2.3 ROM Messages Printing Control 775
    11.2.4 JTAG Signal Source Control 776

12 Interrupt Matrix 777
12.1 Overview 777
12.2 Interrupt Terminology in ESP32-P4 777
    12.2.1 Interrupt 777
    12.2.2 Interrupt Signal/Interrupt Source 777
    12.2.3 Interrupt Flow in ESP32-P4 778
12.3 Features 778
12.4 Functional Description 779
    12.4.1 Peripheral Interrupt Sources 779
    12.4.2 Assign Peripheral Interrupt Source to HP CPU Interrupt 786
        12.4.2.1 Assign One Peripheral Interrupt Source (SOURCE) to HP CPUx 786
        12.4.2.2 Assign Multiple Peripheral Interrupt Sources (SOURCE) to HP CPUx 786
        12.4.2.3 Disable HP CPUx Peripheral Interrupt Source (SOURCE) 786
    12.4.3 Query Current Interrupt Status of HP CPUx Peripheral Interrupt Source 786
    12.4.4 Interrupt Remapping 786
12.5 Register Summary 788
    12.5.1 HP CPU0 Interrupt Matrix Register Summary 788
    12.5.2 HP CPU1 Interrupt Matrix Register Summary 793
12.6 Registers 800
```