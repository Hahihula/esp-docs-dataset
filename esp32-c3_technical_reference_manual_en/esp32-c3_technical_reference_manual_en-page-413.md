

```markdown
Chapter 15 World Controller (WCL)

GoBack

Chapter 15

World Controller (WCL)

15.1 Introduction

ESP32-C3 allows users to allocate its hardware and software resources into Secure World (World0) and Non-secure World (World1), thus protecting resources from unauthorized access (read or write), and from malicious attacks such as malware, hardware-based monitoring, hardware-level intervention, and so on. CPUs can switch between Secure World and Non-secure World with the help of the World Controller.

By default, all resources in ESP32-C3 are shareable. Users can allocate the resources into two worlds by managing respective permission (For details, please refer to Chapter 14 Permission Control (PMS)). This chapter only introduces the World Controller and how CPUs can switch between worlds with the help of World Controller.

15.2 Features

ESP32-C3’s World Controller:

* Controls the CPUs to switch between the Secure World and Non-secure World
* Logs CPU’s world switches

15.3 Functional Description

With the help of World Controller, we can allocate different resources to the Secure World and the Non-secure World:

* Secure World (World0):
  - Can access all peripherals and memories;
  - Performs all security related operations, such user authentication, secure communication, and data encryption and decryption, etc.
* Non-secure World (World1):
  - Can access some peripherals and memories;
  - Performs other operations, such as user operation and different applications, etc.

ESP32-C3’s CPU and slave devices are both configurable with permission to either Secure World and/or Non-Secure World:

* CPU can be in either world at a particular time:
```