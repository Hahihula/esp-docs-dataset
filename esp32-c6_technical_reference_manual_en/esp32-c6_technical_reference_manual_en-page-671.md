

```markdown
Chapter 21 HMAC Accelerator (HMAC) | GoBack

Figure 21.3-2. HMAC Structure Schematic Diagram

Key(K) → Padded key (Kc) → ipad  
          ↓ XOR                     ↓  
opad → XOR                      Message  
          ↓                        ↓  
S2 ──┬── H1                    SHA-256  
     │                          ↓  
     1024-bit                 H1  
     │                          ↓  
     SHA-256                  Hash result

Espressif Systems    671    ESP32-C6 TRM (Version 1.1)  
Submit Documentation Feedback
```