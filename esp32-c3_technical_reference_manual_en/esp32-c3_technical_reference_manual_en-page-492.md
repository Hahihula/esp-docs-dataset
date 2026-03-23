

```markdown
Chapter 19 HMAC Accelerator (HMAC)

GoBack

Figure 19.3-2. HMAC Structure Schematic Diagram

Key (K) → Padded key (Kc)  
    ↓ ipad  
    ↓ XOR  
    S1 + Message → SHA-256 → H1  

opad ↓ XOR  
    S2 || H1 (1024-bit) → SHA-256 → Hash result

Espressif Systems
492
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```