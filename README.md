# eXpOS – Experimental Operating System

An educational operating system built from scratch as part of the [eXpOS (Experimental Operating System)](https://exposnitc.github.io/) project developed by National Institute of Technology Calicut.

The repository contains implementations of:

- **eXpOS** running on the **XSM (Experimental String Machine)** architecture simulator
- **neXpOS**, a dual-core extension of eXpOS running on the **NEXSM** architecture simulator

Official references:
- [Documentation](https://exposnitc.github.io/documentation.html)
- [Roadmap](https://exposnitc.github.io/expos-docs/roadmap/)

---

## Overview

This project was completed as part of an Operating Systems laboratory course and involved implementing core operating system components from scratch, including:

- Process management
- Memory management
- File systems
- Interrupt and exception handling
- System calls
- CPU scheduling
- Synchronization primitives
- Multi-user support
- Disk management
- Shell and user programs
- Dual-core execution support

The operating system is developed using:
- **SPL (System Programming Language)** for kernel modules
- **ExpL (Experimental Language)** for user programs

Both systems run on the XSM/NEXSM architecture simulators provided by the eXpOS project.

---

## Project Architecture

```
+--------------------------------------------------+
|                User Programs (ExpL)              |
+--------------------------------------------------+
|                eXpOS Library                     |
+--------------------------------------------------+
|                  eXpOS Kernel                    |
|  - Scheduler                                     |
|  - Memory Manager                                |
|  - File System                                   |
|  - Process Manager                               |
|  - Device Handlers                               |
+--------------------------------------------------+
|             XSM Machine Simulator                |
+--------------------------------------------------+
```

---

## Features Implemented

- Process Management
  - Process creation and termination
  - Context switching
  - Round-robin scheduling
  - Multi-process execution
  - Process table management
- Memory Management
  - Paging-based memory management
  - Page table handling
  - Heap and stack management
  - Shared library loading
- File System
  - File creation and deletion
  - File read/write operations
  - Inode management
  - Disk block allocation
  - Root file system support
- Interrupts & Exceptions
  - Timer interrupt handling
  - Console interrupt handling
  - Exception handling routines
  - System call interface
- Synchronization
  - Process synchronization using semaphores
  - Resource sharing management
  - Concurrency control mechanisms
- Dual Core Architecture Support
  - Dual-core execution support on NEXSM
  - Parallel process scheduling
  - Shared memory coordination between cores
  - Inter-processor synchronization
  - Kernel support for concurrent execution
- User Programs
  - Shell implementation
  - Basic command execution
  - User-level applications in ExpL

---

## Key Concepts Explored

- Operating system internals
- Process scheduling and context switching
- Paging and memory management
- Synchronization and concurrency control
- Dual-core kernel execution
- Interrupt-driven execution
- File system implementation
- Low-level system programming
- Assembly-level debugging

---

## Installation and Setup

- To clone the repo and open it:
```
git clone https://github.com/HattoriMan/OS_Lab.git
cd OS_Lab
```
- For setup of the ExpL and SPL compilers as well as the libraries and other installations required for it to work follow from Stage 1 listed in the roadmap. There is a `setup.sh` file in *Stage_01* folder which also does the installation.
- The project can be reproduced by following the official eXpOS roadmap from Stage 1 onward. 

---

## Important Notes

- All files required to build the OS up to a particular stage are included in the corresponding stage directory of my implementation.
- Only files modified or newly added have been pushed till *Stage_24* (including it).
- All stages from *Stage_25* onward contain the complete set of SPL and ExpL source files, not just the modified or newly added ones.
- For easier compilation a `compile` bash script has been written for *Stage_25* and above which compiles all the files in the stage. You can change the directory location constants in it according to your setup.
- *Stages_25* to *Stage_28* contains `run_comms` file which contains the command to be executed in the `xfs-interface` to load the files but it might depend on your setup.
- *Stage_28* contains the implementation of *neXpOS*, a dual-core operating system running on the *NEXSM architecture*.