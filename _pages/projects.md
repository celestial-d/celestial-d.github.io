---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true

---

My work focuses on system behavior understanding, testing, and debugging:

* Implications of Non-Volatile Memories

    Non-volatile memory (NVM) technologies, including flash-based solid-state drives (SSD) and byte-addressable persistent memories (PM) have a great impact on modern       storage system. Unfortunately, building a robust modern system with such new devices is time-consuming since the software stack changed aggressively, and it is hard   to understand system behavior correctly. We collect kernel bug cases,and leverage modern technologies such as virtual machine and static analysis to explore the system:
    1. We collected persistent memory related patches in the Linux kernel tree automatically and analyzed patches in detail, Through the study, we extract several implcations of persistent memory bugs.
    2. We leveraged Virtual Machine (QEMU) to reproduce persistent memory related bug cases and provided extra plugins to improve debugging support.
    3. We leveraged static analyzer (LLVM) to perform inter and intra function analysis to test persistent memory drivers and found out several potential vulnerabilities.
    4. We leveraged existing persistent memory bug cases to evaluate different persistent memory emulation method and identified potential emulation problem.
    5. We leveraged Virtual Machine to emulate power failure to test crash consistency issues in non-volatile memory system, and identified multiple vulnerabilities.
      
    [Editing a markdown file for a talk](/images/editing-talk.png)

* Local File System (e.g, EXT4 and XFS) & Utilities

    Local file system are stilla key component in storage system. To accommodate modern system and application requirements, local file system added multiple features  and changed aggressively. Such varies contribute to multiple vulnerabilities, and may result in unexpected behaviors such as data loss, server's downtime and system crash. We did multiple study and testing in different aspects:
   1. We collected local file system bug cases in Bugzilla and Linux kernel source tree, then we reproduce some of real-world system failure. Through our experiments and detailed analysis, we concluded several key features that affect reproducibility of bug cases.
   2. We leveraged existing tracers such as strace, ftrace, systemTap and perf to capture kernel function level info. At the same time, we rely on scsi-tool to capture device commands. Based on these two types of info, we identified the relationship between them and provided a new cross-layer dianogis method.
   3. We modified virtual machine structure to capture device commands and instructions, and performed a full-stack and novel cross-layer diagnosis method. OUr experiments shows that the diagnosis method can help developers spend less time understanding the system behavior and pinpoint the root casue.
   4. We leveraged static analysis (LLVM) to extract file system configuration dependencies, then we perform testing with five different modified exisinting tools. The experiments explore several local file system issues.

* Parallel File System (e.g., BeeGFS)

    Parallel storage systems are deployed widely in data centers and national labs to empower data-intensive computing. However, correctness issues and scalablity issues may still result in several unexpected behaviors such as data loss and system hang. We build a framework to perform a taxonomy for parallel file system:
    1. We explored the PFSes structure and bug cases, then identified several potencial scenarios.
    2. We designed experiments to generate inconsistency mapping potencial scenarios and check whether PFSes can response correctly and perform correct recovery.
   


