

```markdown
be automatically cleared to 0, and software needs to be enabled again in the interrupt/exception service routine. This register should be configured before turning on the global interrupt enable.

3. Enable the global interrupt enable.
4. Execute the interrupt programs.
5. Disable CPU global interrupt enable.
6. Read Field `WCL_CORE_O_FROM_ENTRY_A` for Entry A:

    * 32: indicates all interrupts are handled, and return to a normal program,
        (a) Update Field `WCL_CORE_O_CURRENT_A` of Entry A to 0, indicating the CPU is no longer at the interrupt monitored at Entry A.
        (b) Go to Step 7.

    * 0~31: indicates the CPU returns to another interrupt monitored at Entry B,
        - Update the world switch register of Entry A:
            * Update Field `WCL_CORE_O_CURRENT_A` to 0, indicating the CPU is no longer at the interrupt monitored at Entry A.
            * Fields `WCL_CORE_O_FROM_WORLD_A` and `WCL_CORE_O_FROM_ENTRY_A` stay the same.
        - Update the world switch register of Entry B:
            * Update Field `WCL_CORE_O_CURRENT_B` to 1, indicating the CPU will return to Entry B.

7. Prepare to exit interrupt.
    (a) Check if CPU needs to switch to the other world:
        * If world switch not required, then go to Step 8.
        * If world switch required, then switch the CPU to the other world following instructions described in Section 15.4, then go to Step 8.

8. Enable interrupts, restore context and exit.

Note:

Steps 6 and 7 should not be interrupted by any interrupts. Therefore, users need to disable all the interrupts before these steps, and enable interrupts once done.
```