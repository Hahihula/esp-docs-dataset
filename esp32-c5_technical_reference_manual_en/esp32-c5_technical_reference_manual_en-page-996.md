

```markdown
Chapter 31 Key Manager

GoBack

![Figure 31.6-2. ECDHO Deploy Mode](image)

Detailed Process

1. Generate locally k1 and calculate k1 * G.
2. Complete the key deployment in Key Manager:
   (a) Write k1 * G to the internal memory of the Key Manager.
   (b) Wait for the Key Manager to complete the deployment.
   (c) Read k2 * G and key_info (corresponding to the negotiated private key k1 * k2 * G) from the internal memory of the Key Manager by specifying the address.
3. Generate the negotiated key k1 * k2 * G by using k2 * G together with the local private key k1.

Note:
- The ECDHO Deploy Mode ensures that the negotiated private key is generated only locally by the user and internally by the Key Manager. Any data leakage during the deployment process will not result in the leakage of the negotiated private key. Therefore, data transmission in this mode can occur in an untrusted environment.
- In ECDHO Deploy Mode, the negotiated private key can only be obtained after running the Key Manager. This mode is not suitable for scenarios where the exact value of the private key needs to be known in advance.

31.6.2.4 ECDH1 Deploy Mode

Users can use this mode to deploy a negotiated private key.
```

```markdown
Espressif Systems                           996                          ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```