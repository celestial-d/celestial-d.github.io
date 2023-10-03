---
permalink: /
title: ""
excerpt: "home"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! I'm Duo Zhang, a Ph.D. candidate in [Data Storage Lab](https://www.ece.iastate.edu/~mai/lab/dsl.html) at Iowa State University. I'm interested in all things involving the storage system. 

For more information, please click here for the [Curriculum Vitae](https://github.com/celestial-d/celestial-d.github.io/blob/master/files/CV.pdf)

My current research interests focus on exploration of **bug reproducibility** and the **reliability** issues of the **storage system** with advanced storage technologies (e.g., persistent memory, CXL). Specifically, I am interested in developing noval system testing frameworks through state-of-the-art tools (i.e., virtual machines (QEMU), tracers(e.g., kprobe) and static analysis (LLVM)).

<h2 id="News">News!</h2>

- **[09/2023] I expect to graduate in Dec. 2023 and am looking for a full time position!**
- [05/2023] One paper to appear in ACM TOS! Thank the reviewers for constructive feedback!
- [02/2023] One paper accepted in NVMW'23! Thank the reviewers for constructive feedback!
- [12/2022] One paper on file systems accepted in FAST'23! Thank the reviewers for constructive feedback!

<h2 id="Education">Education</h2>

* Ph.D in Ames, Iowa State University, 2023 (expected)
* M.S. in Syracuse, Syracuse University, 2018
* B.Eng. in Beijing, Beijing Union University, 2014


<h2 id="Publications">Selected Publications</h2>

Please check a full list at [Google Scholar Page](https://scholar.google.com/citations?hl=en&user=QXwhPMkAAAAJ)

- "Analyzing Configuration Dependencies of DAX File Systems",
Tabassum Mahmud, Om Rameshwar Gatla, **Duo Zhang**, Carson Love, Ryan Bumann, and Mai Zheng, Iowa State University. Proceedings of the 14th Annual Non-Volatile Memories Workshop (NVMW), 2023

- "On the Scalability of Testing the Crash Consistency of PM Systems", **Duo Zhang**, Om Rameshwar Gatla, and Mai Zheng, Iowa State University; Abdullah Al Raqibul Islam, and Dong Dai, University of North Carolina at Charlotte. Proceedings of the 21th USENIX Conference on File and Storage Technologies (FAST-WIP), 2023

- "ConfD: Analyzing Configuration Dependencies of File Systems for Fun and Profit",
 Tabassum Mahmud, Om Rameshwar Gatla, **Duo Zhang**, Carson Love, Ryan Bumann, Mai Zheng. Proceedings of the 21st USENIX Conference on File and Storage Technologies (FAST), 2023

- "On the Reproducibility of Bugs in File-System Aware Storage Applications",
 **Duo Zhang**, Tabassum Mahmud, Om Rameshwar Gatla, Runzhou Han, Yong Chen and Mai Zheng. Proceedings of the 16th International Conference on Networking, Architecture, and Storage (NAS), 2022

- "Understanding Configuration Dependencies of File Systems", 
  Tabassum Mahmud, **Duo Zhang**, Om Rameshwar Gatla, Mai Zheng. Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage), 2022
  
- "Benchmarking for observability: The case of diagnosing storage failures",
 **Duo Zhang**, Mai Zheng. BenchCouncil Transactions on Benchmarks (TBench), 2021

- "A study of persistent memory bugs in the Linux kernel", **Duo Zhang**, Om Rameshwar Gatla, Wei Xu, Mai Zheng. Proceedings of the 14th ACM International Conference on Systems and Storage (SYSTOR), 2021

- "Fingerprinting the Checker Policies of Parallel File Systems", Runzhou Han, **Duo Zhang**, Mai Zheng. IEEE/ACM Fifth International Parallel Data Systems Workshop (PDSW), 2020

- "On Failure Diagnosis of the Storage Stack",
**Duo Zhang**, Om R. Gatla, Runzhou Han, Mai Zheng.
Proceedings of the 12th USENIX Workshop on Hot Topics in Storage and File Systems (HotStorage-P), 2020	

- "A Cross-Layer Approach for Diagnosing Storage System Failures",
**Duo Zhang**, Chander Bhushan Gupta, and Mai Zheng, Iowa State University; Adam Manzanares, Filip Blagojevic, and Cyril Guyot, Western Digital Research. 
Proceedings of the 18th USENIX Conference on File and Storage Technologies (FAST-WIP), 2020

<h2 id="Teaching">Teaching</h2>

- CPRE308 Operating Systems Principles and Practice, Guest Lecturer & Teaching Assistant (FA’21,
SP’22, FA’22, SP’23, FA’23)
- CPRE563X Advanced Data Storage Systems, Guest Lecturer & Teaching Assistant (SP’22)

<h2 id="Service">Service</h2>

* IEEE IPDPS 2021 reviewer
* IEEE SECON 2019 reviewer
* IEEE INFOCOM 2019 reviewer
* IEEE VNC 2018 reviewer

<h2 id="Research">Research Projects</h2>

My work focuses on system behavior understanding, testing, and debugging:

* Non-Volatile Memories
![Non-Volatile Memories](/images/nvm.jpg)
    Non-volatile memory (NVM) technologies, such as flash-based solid-state drives (SSD) and byte-addressable persistent memories (PM), wield significant influence over contemporary storage systems. Regrettably, constructing a resilient modern system incorporating these innovative devices is a time-consuming endeavor due to the radical changes in the software stack and the complexity of accurately comprehending system behavior. To address these challenges, our approach entails the aggregation of kernel bug cases, along with the utilization of cutting-edge technologies like virtual machines and static analysis for system analysis:
    1. We automated the collection of patches related to persistent memory within the Linux kernel tree and subjected these patches to in-depth analysis. This comprehensive study allowed us to extract various insights into persistent memory bugs, subsequently contributing to the development of multiple persistent memory system bug detection methodologies.
    2. We leveraged virtual machine (QEMU) to reproduce persistent memory-related bug cases and provided extra plugins to improve debugging support.
    3. Employing a static analyzer based on LLVM, we conducted both inter and intra function analyses to scrutinize persistent memory drivers, thereby uncovering several potential vulnerabilities.
    4. Leveraging pre-existing persistent memory bug cases, we evaluated various methods of emulating persistent memory and identified potential emulation-related challenges.
    5. Employing virtual machines, we simulated power failures to examine crash consistency issues within non-volatile memory systems. This investigation led to the identification of multiple vulnerabilities in this context.

* Local File System (e.g, EXT4 and XFS) & Utilities
![Local File System](/images/local.jpg)
    Local file systems remain a pivotal component of storage systems. To align with the demands of modern systems and applications, local file systems have undergone significant evolution, introducing numerous features. However, these changes have given rise to multiple vulnerabilities and the potential for unforeseen consequences, such as data loss, server downtime, and system crashes. Our comprehensive approach encompasses studies and testing across various dimensions:
   1. We initiated our efforts by amassing instances of local file system issues from Bugzilla and the Linux kernel source tree. Subsequently, we recreated select real-world system failures. Our experiments, coupled with detailed analyses, culminated in the identification of several pivotal reproducibility patterns within these issue cases.
   2. To gain insights at the kernel level, we harnessed established tracers like Strace, FTrace, SystemTap, and perf to capture relevant system data. Additionally, we employed scsi-tool to record device commands. This dual-source information allowed us to introduce a novel cross-layer diagnostic method.
   3. Our innovation extended to modifying the virtual machine structure to capture device commands and instructions. This led to the development of a comprehensive, cross-layer diagnostic approach that covers the entire stack. Our experiments corroborated the effectiveness of this method, as it streamlines the process of comprehending system behavior and isolating root causes.
   4. Leveraging static analysis by LLVM, we systematically extracted dependencies within file system configurations. Subsequently, we conducted testing using five different adapted existing tools. These experiments were instrumental in uncovering various local file system issues.

* Parallel File System (e.g., BeeGFS)
![Parallel File System](/images/pfs.jpg)
    Parallel storage systems find extensive deployment in data centers and national laboratories, facilitating data-intensive computing tasks. Nonetheless, issues related to correctness and scalability can lead to unforeseen problems, such as data loss and system unresponsiveness. To address these concerns, we have developed a framework for conducting a taxonomy of parallel file systems:
    1. Our initial step involved a thorough examination of the structures and documented bug cases within parallel file systems. This analysis allowed us to pinpoint several potential scenarios of concern.
    2. Subsequently, we devised a series of experiments aimed at generating inconsistency scenarios and assessing the ability of parallel file systems to respond appropriately and execute correct recovery procedures.

<h2 id="Contact">Contact</h2>

* E-mail: duozhang [at] iastate.edu
* Linkedin: [link](https://www.linkedin.com/in/duo-zhang-b31344133/)
