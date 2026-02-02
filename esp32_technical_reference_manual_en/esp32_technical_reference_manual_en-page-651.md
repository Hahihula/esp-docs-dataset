**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Subtitle:**
29.3.1.3 Operator Submodule

**Diagram Description:**
- The diagram is labeled "Figure 29.3-3. Operator Submodule".
- It shows a block with inputs and outputs related to the operator submodule.
- Inputs include:
  - timer 0 status
  - timer 1 status
  - timer 2 status
- Outputs are directed towards "PWMx A" or "PWMx B", labeled as "OPERATOR x".

**Text:**
"The configuration parameters of the operator submodule are shown in Table 29.3-1."

**Table Title and Description:**
- **Title:** Table 29.3-1. Configuration Parameters of the Operator Submodule
- The table is titled "Configure the parameter options for PWMxA and/or PWMxB output."
- It lists various parameters with descriptions:
  - Set up at which time the timing events occur.
  - Define what action should be taken on timing events (e.g., switch high or low, toggle outputs).
  - Use direct software control to force state of PWM outputs.
  - Add a dead time for raising and/or failing edge on PWM outputs.

**Footer:**
- "Espressif Systems"
- Page number: 651
- Document version: ESP32 TRM (Version 5.6)
- Links: Submit Documentation Feedback