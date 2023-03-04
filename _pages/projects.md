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
    3. We leveraged static analyzer(LLVM) to perform inter and intra function analysis to test persistent memory drivers and found out several potential vulnerabilities.
    4. We leveraged existing persistent memory bug cases to evaluate different persistent memory emulation method and identified potential emulation problem.
    5. We leveraged Virtual Machine to emulate power failure to test crash consistency issues in non-volatile memory system, and identified multiple vulnerabilities.
      
    Example: editing a markdown file for a talk ![Editing a markdown file for a talk](/images/editing-talk.png)

* Local File System (e.g, EXT4 and XFS) & Utilities

    _Duo Zhang_, Om Rameshwar Gatla, and Mai Zheng, Iowa State University; Abdullah Al Raqibul Islam, and Dong Dai, University of North Carolina at Charlotte. 
    Proceedings of the 21th USENIX Conference on File and Storage Technologies (FAST-WIP), 2023

* Parallel File System (e.g., BeeGFS)

    _Duo Zhang_, Om Rameshwar Gatla, and Mai Zheng, Iowa State University; Abdullah Al Raqibul Islam, and Dong Dai, University of North Carolina at Charlotte. 
    Proceedings of the 21th USENIX Conference on File and Storage Technologies (FAST-WIP), 2023


