

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA)    GoBack


(a) Compute the point $(x, y) = kG$
(b) Calculate $r = x \bmod n$. If $r$ is equal to zero, return to the previous step and select a new random value of $k$.
(c) Calculate $s = k^{-1} * (z + d*r) \bmod n$. If $s$ is equal to zero, return to step 4 and select a new random value of $k$.
(d) The signature is the pair $(r, s)$.

6. Send the message $m$ and signature $(r, s)$ to the recipient.


28.3.4 Signature Verification

The recipient can then use the public key associated with the private key used for signature generation to verify the signature. The verification process involves checking that the signature was generated using the correct private key and that the signature is valid for the given message.

The ECDSA signature verification process is described below:

1. Obtain public key $Q$ and receive the message $m$ and signature $(r, s)$.
2. Calculate the hash of the message $e$: $e$ is equal to HASH($m$), where HASH is a cryptographic hash function, such as SHA-256.
3. Compute the digest of the message $z$: Let $z$ be the $L_n$ leftmost bits of $e$, where $L_n$ is the bit length of the base point order $n$.
4. Verify the signature: The signature is verified as follows:
   (a) Verify that $r$ and $s$ are integers between 1 and $n-1$, where $n$ is the order of the base point on the elliptic curve. If either $r$ or $s$ is outside of this range, the signature is invalid.
   (b) Calculate $u_1 = z * s^{-1} \bmod n$ and $u_2 = r * s^{-1} \bmod n$.
   (c) Calculate the point $(x_1, y_1) = u_1*G + u_2*Q$, where $G$ is the base point on the elliptic curve, and $Q$ is the public key associated with the private key used for signature generation.
   (d) Verify that $r = x_1 \bmod n$. If $r$ is not equal to $x_1 \bmod n$, the signature is invalid.

5. Accept or reject the signature: If the signature is valid, the recipient can be confident that the message was not tampered with and that it came from the expected sender, thus can accept the message as authentic. Otherwise, the recipient rejects the message as invalid.


28.4 Functional Description

This section describes the details of ESP32-C5’s ECDSA accelerator.

28.4.1 ECDSA Working Modes

The ECDSA accelerator integrated in the ESP32-C5 has three working modes, which are Signature Generation, Signature Verification and Public Key Export modes.

Users can select the working mode for the ECDSA accelerator by configuring `ECDSA_WORK_MODE` according to Table 28.4-1 below.
```