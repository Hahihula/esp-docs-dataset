

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA)    GoBack


# Chapter 28

## Elliptic Curve Digital Signature Algorithm (ECDSA)

### 28.1 Introduction

In cryptography, the Elliptic Curve Digital Signature Algorithm (ECDSA) offers a variant of the Digital Signature Algorithm (DSA) which uses elliptic-curve cryptography.

ESP32-C5’s ECDSA accelerator provides a secure and efficient environment for computing ECDSA signatures. It offers fast computations while ensuring the confidentiality of the signing process to prevent information leakage. This makes it a valuable tool for applications that require high-speed cryptographic operations with strong security guarantees. By using the ECDSA accelerator, users can be confident that their data is protected without sacrificing performance.

### 28.2 Features

ESP32-C5’s ECDSA accelerator supports:

- Digital signature generation and verification
- Three different elliptic curves, namely, P-192, P-256, and P-384 defined in FIPS 186-5
- Multiple hash algorithms for message hash in the ECDSA operation, including SHA-224, SHA-256, SHA-384, SHA-512, SHA-512-224, and SHA-512-256, defined in FIPS PUB 180-4 Spec
- State-dependent register access control in different operation states to ensure information security

### 28.3 ECDSA Basics

#### 28.3.1 Domain Parameters

ECDSA uses parameters that define the elliptic curve over a finite field, as well as the generator point and the order of the base point. These parameters are usually referred to as domain parameters, and they are required for key generation, signature generation, and signature verification.

The domain parameters used in ECDSA consist of the following:

- The elliptic curve domain parameters, which include:
  - The prime modulus p, which specifies the size of the finite field over which the elliptic curve is defined.
  - The coefficients a and b, which specify the elliptic curve equation.
  - The base point G on the curve, which can be used to generate public keys.
```