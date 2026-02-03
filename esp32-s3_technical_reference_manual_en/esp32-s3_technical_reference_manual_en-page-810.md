**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Heading:**
3. Disable all interrupts.

**Body Text with Steps and Annotations:**

4. Update the address where the interrupt at Entry A returns to:

   - Read Field WCL CORE m FROM ENTRY A for Entry A:
     - **0:** indicates all interrupts are handled, and returns to a normal program.
       (a) Update Field WCL CORE m CURRENT A of Entry A to 0, indicating the CPU is no longer at the interrupt monitored at Entry A.

   Go To Step B

- 1 – 13: indicates the CPU returns to another interrupt monitored at Entry:
   - **(a)** First, check the return address of the interrupt at Entry:

     * If it points to the first NOP.N instruction of the interrupt at Entry B,
       then add 4 to the return address of the interrupt at Entry A.

     * If it points to the second NOP.N instruction of the interrupt at Entry
       (a), 
       **then** add 2 to the return address of the interrupt at Entry

   - **(b)** Update the How to Read World Switch Registers:

     * Update the world switch register of Entry A:
       - Update Field WCL CORE m CURRENT A to 0, indicating the CPU is no longer at the interrupt monitored at Entry.
       - Fields WCL CORE m FROM WORLD A and WCL CORE m FROM ENTRY stay
         **A** same.

   - **(b)** Update the world switch register of Entry B:
     * Update Field WCL CORE m CURRENT B to 1, indicating the CPU will return to Entry

5. Prepare to exit interrupt:

   (a) Check if CPU needs to switch to the other world.
       - If world switch not required, then go to Step
       **6**.

   - If world switch required,
     * then switch the CPU to the other world following instructions described in Section 16.4,

6. Enable interrupts and exit

**Note:**
Steps should be interrupted by any interrupts.
Therefore users need disable all before these steps, enable once done.


**Footer Information:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)