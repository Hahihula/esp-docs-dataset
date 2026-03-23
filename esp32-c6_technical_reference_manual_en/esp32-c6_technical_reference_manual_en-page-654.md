

```markdown
Chapter 20 ECC Accelerator (ECC)

## Chapter 20

### ECC Accelerator (ECC)

#### 20.1 Introduction

Elliptic Curve Cryptography (ECC) is an approach to public-key cryptography based on the algebraic structure of elliptic curves. ECC allows smaller keys compared to RSA cryptography while providing equivalent security.

ESP32-C6's ECC Accelerator can complete various calculations based on different elliptic curves, thus accelerating the ECC algorithm and ECC-derived algorithms (such as ECDSA).

#### 20.2 Features

ESP32-C6's ECC Accelerator has the following features:

* Two different elliptic curves, namely P-192 and P-256 defined in [FIPS 186-3](#)
* Six working modes
* Interrupt upon completion of calculation

#### 20.3 Terminology

This section covers terminology used to describe ECC Accelerator.

##### 20.3.1 ECC Basics

###### 20.3.1.1 Elliptic Curve and Points on the Curves

The ECC algorithm is based on elliptic curves over prime fields, which can be represented as:

```math
y^2 = x^3 + ax + b \mod p
```

where,

* `p` is a prime number.
* `a` and `b` are two non-negative integers smaller than `p`.
* `(x, y)` is a point on the curve satisfying the representation.

###### 20.3.1.2 Affine Coordinates and Jacobian Coordinates

An elliptic curve can be represented as below:
```