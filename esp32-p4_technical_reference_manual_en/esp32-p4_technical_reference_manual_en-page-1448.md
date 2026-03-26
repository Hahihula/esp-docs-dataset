

# Chapter 26

## ECC Accelerator (ECC)

### 26.1 Overview

Elliptic Curve Cryptography (ECC) is an approach to public-key cryptography based on the algebraic structure of elliptic curves. ECC uses smaller keys compared to RSA cryptography while providing equivalent security.

ESP32-P4's ECC accelerator can complete various calculations based on different elliptic curves, thus accelerating the ECC algorithm and ECC-derived algorithms such as ECDSA.

### 26.2 Feature List

ESP32-P4's ECC accelerator has the following features:

*   Three different elliptic curves, namely, P-192, P-256, and P-384 defined in [FIPS 186-5](#)
*   11 working modes
*   Enhanced anti-attack performance
*   Interrupt upon completion of calculation

### 26.3 ECC Basics

To better illustrate the functionality of the ECC accelerator, the basic knowledge and terminology used in this chapter are introduced in this section.

#### 26.3.1 Elliptic Curve and Points on the Curves

The ECC algorithm is based on elliptic curves over prime fields, which can be represented as:

$$y^2 = x^3 + ax + b \mod p$$

where,

*   $p$ is a prime number,
*   $a$ and $b$ are two non-negative integers smaller than $p$,
*   and $(x,y)$ is a point on the curve satisfying the representation.