**Chapter Title:**
Chapter 16

**Subheading and Section Titles:**
- World Controller (WCL)
- Introduction
- Features
- Functional Description

**Body Text:**

ESP32-S3 allows users to allocate its hardware and software resource into Secure World (World0) and Non-secure World (World1), thus protecting resource from unauthorized access (read or write), and from malicious attacks such as malware, hardware-based monitoring, hardware-level intervention, and so on. CPUs can switch between Secure World and Non-secure World with the help of the World Controller.

By default, all resource in ESP32-S3 are shareable. Users can allocate the resource into two worlds by managing respective permissions (For details, please refer to Chapter 15 Permission Control (PMS)). This chapter only introduces the World Controller and how CPUs can switch between worlds with the help of World Controller.

**Subheading: Features**

ESP32-S3’s World Controller:
- Controls the CPUs to switch between the Secure World and Non-secure World
- Logs CPU's world switches
- Allows NMI masking
- Allows independent world switches of CPUs (CORE_m: CPU0 and CPU1)

**Subheading: Functional Description**

With the help of World Controller, we can allocate different resources to the Secure World and the Non-secure World:

- **Secure World (World0):**
  - Can access all peripherals and memories;
  - Performs all confidential operations, such as fingerprint identification, password processing, data encryption and decryption, security authentication, etc.

- **Non-secure World (World1):**
  - Can access some peripherals and memories;
  - Performs other operations, such as user operation and different applications, etc.