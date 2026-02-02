**Chapter Title:**
Chapter 2 DMA Controller (DMA)

**Section Heading and Subsection with Content:**

- **Subsection Header:** All high-speed communication modules powered by DMA

- **Main Section Header:** 
  - Functional Description
  
    **Body Text:**
    All modules that require high-speed data transfer in bulk contain a DMA controller. DMA addressing uses the same data bus as the CPU to read/write to the internal RAM.

    Each DMA controller features different functions. However, the architecture of the DMA engine (DMA_ENGINE) is the same in all DMA controllers.
  
- **Subsection Header:** 
  - DMA Engine Architecture
  
    **Image Description:**
    Figure 2.3-1 shows a block diagram labeled "Figure 2.3-1. DMA Engine Architecture" with components such as RAM, AHB BUS, and various links (out_link0 to out_linkn) connected in sequence.

    **Body Text:**
    The DMA Engine accesses SRAM over the AHB BUS. In Figure 2.3-1, the RAM represents the internal SRAM banks available on ESP32. Further details on the SRAM addressing range can be found in Chapter 3 System and Memory. Software can use a DMA Engine by assigning a linked list to define the DMA operational parameters.

    The DMA Engine transmits the data from the RAM to a peripheral, according to the contents of the out_link descriptor. Also, the DMA Engine stores the data received from a peripheral into a specified RAM location, according to the contents of the in_link descriptor.
  
- **Subsection Header:** 
  - Linked List
  
    **Image Description:**
    Figure 2.3-2 shows "Figure 2.3-2. Linked List Structure" with fields labeled as follows:
    
    | DW0   | owner | eof | reserved | length | size |
    |-------|-------|-----|----------|--------|------|
    | DW1   |       |     |          | buffer address pointer |
    | DW2   |       |     |          | next descriptor address |

    **Body Text:**
    The DMA descriptor’s linked lists (out_link and in_link) have the same structure. As shown in Figure 2.3-2, a linked-list descriptor consists of three words. The meaning of each field is as follows:
    
    - DW0 owner
    - DW1 buffer address pointer
    - DW2 next descriptor address

**Footer:**
Espressif Systems  
57 ESP32 TRM (Version 5.6)  

**Link Text:** Submit Documentation Feedback