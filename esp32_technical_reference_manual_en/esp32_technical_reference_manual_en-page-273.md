Title: Chapter 13 Process ID Controller (PID)

Table Title:
- Table 13.3-3. Configuration of PIDCTRLFROM_N_REG

Table Content:

| [6:3] Previous interrupt | [2:0] Previous process |
|---------------------------|-------------------------|
| O                         | No interrupt            | 0                          | Process with PID of 0 |
| 1                         | Level 1 Interrupt      | 1                          | Process with PID of 1 |
| 2                         | Level 2 Interrupt      | 2                          | Process with PID of 2 |
| 3                         | Level 3 Interrupt      | 3                          | Process with PID of 3 |
| 4                         | Level 4 Interrupt      | 4                          | Process with PID of 4 |
| 5                         | Level 5 Interrupt      | 5                          | Process with PID of 5 |
| 6                         | Level 6 Interrupt      | 6                          | Process with PID of 6 |
| 7                         | Level 7 Interrupt      | 7                          | Process with PID of 7 |

Body Text:
PID Controller possesses registers PIDCTRLFROM_1_REG ~ PIDCTRLFROM_7_REG, which correspond to the interrupts of Level 1, Level 2, Level 3, Level 4, Level 5, Level 6 (Debug), and NMI respectively. This enables the system to implement interrupt nesting. Please refer to Table 13.3-1 for examples.

If the configuration of register PIDCTRLINTERRUPT_ENABLE_REG prevents PID Controller from identifying an interrupt, PID Controller will not record any information, and PIDCTRLLEVEL_REG and PIDCTRLFROM_N_REG will remain unchanged.

Subtitle: 13.3.3 Proactive Process Switching

Body Text:
As mentioned before, only an elevated process with PID of O/1 can initiate a process switch. The new process may have any PID from 0 ~ 7 after the process switch. The key for successful proactive process switching is that when the last command of the current process switches to the first command of the new process, PID should switch from 0/1 to that of the new process.

The software procedure for proactive process switching is as follows:

- Mask all the interrupts except NMI by using software.
- Set register PIDCTRL_NMI_MASK_ENABLE_REG to 1 to generate a CPU NMI Interrupt Mask signal.
- Configure registers PIDCTRL_PID_DELAY_REG and PIDCTRL_NMI_DELAY_REG.
- Configure register PIDCTRL_PID_NEW_REG.
- Configure register PIDCTRL_LEVEL_REG and PIDCTRLFROM_N_REG.
- Set register PIDCTRL_PID_CONFIRM_REG and register PIDCTRL_NMI_MASK_DISABLE_REG to 1.
- Revoke the masking of all interrupts but NMI.
- Switch to the new process and fetch instruction.

Though we can deal with interrupt nesting, an elevated process should not be interrupted during the process switching, and therefore the interrupts have been masked in step 1 and step 2.

In step 3, the configured values of registers PIDCTRL_PID_DELAY_REG and PIDCTRL_NMI_DELAY_REG will affect step 6.
In step 4, the configured value of register PIDCTRL_PID_NEW_REG will be the new PID after step 6.

Footer:
Espressif Systems
Page Number: 273
Document Version Information (Version 5.6)
Link Text: Submit Documentation Feedback

Navigation Link at Top Right Corner:
GoBack