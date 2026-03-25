

```markdown
Chapter 20 ECC Accelerator (ECC)

## Chapter 20

### ECC Accelerator (ECC)

#### 20.1 Introduction

Elliptic Curve Cryptography (ECC) is an approach to public-key cryptography based on the algebraic structure of elliptic curves. ECC uses smaller keys compared to RSA cryptography while providing equivalent security.

ESP32-H2's ECC accelerator can complete various calculations based on different elliptic curves, thus accelerating the ECC algorithm and ECC-derived algorithms (such as ECDSA).

#### 20.2 Features

ESP32-H2’s ECC accelerator has the following features:

*   2 different elliptic curves, namely P-192 and P-256 defined in [FIPS 186-3](#)
*   11 working modes
*   Interrupt upon completion of calculation

#### 20.3 ECC Basics

To better illustrate the functionality of the ECC accelerator, the basic knowledge and terminology used in this chapter are introduced in this section.

##### 20.3.1 Elliptic Curve and Points on the Curves

The ECC algorithm is based on elliptic curves over prime fields, which can be represented as:

$$y^2 = x^3 + ax + b \mod p$$

where,

*   $p$ is a prime number,
*   $a$ and $b$ are two non-negative integers smaller than $p$,
*   and $(x,y)$ is a point on the curve satisfying the representation.

##### 20.3.2 Affine Coordinates and Jacobian Coordinates

An elliptic curve can be represented as below:
```