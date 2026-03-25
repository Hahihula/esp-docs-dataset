

```markdown
Chapter 25 Elliptic Curve Digital Signature Algorithm (ECDSA)    GoBack

• If no more message block, exit.

Note:
1. In this step, the software can also write the next message block (to be processed) in register ECDSA_MEM_M,
   if any, while the interface starts SHA operation, to save time.
2. You are resuming the ECDSA SHA interface with the previously paused operation.
```