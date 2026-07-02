---

title: "Linux Kernel Modules: Process Table Walker"

date: 2026-07-01

draft: false

---



**TL;DR** — Developed loadable Linux kernel modules (LKM) in C to interact directly with kernel-space memory and traverse the OS process table.



🔗 **Repo:** [github.com/SahibGill386/linux-kernel-modules](https://github.com/SahibGill386/linux-kernel-modules)



### The Build

This was a hands-on Operating Systems coursework project to bridge the gap between user space and kernel space. 



* **Module 1:** A foundational LKM to execute code inside the running kernel, accessing restricted OS values like `jiffies` (system ticks) and the internal `HZ` clock rate.

* **Module 2:** A process-listing module that hooks into `<linux/sched.h>` to walk the kernel's internal linked list of every running process (`task_struct`), mapping live process IDs and state codes directly from memory.



*Note: This is guided academic coursework demonstrating systems-level C programming and kernel architecture, rather than an original research tool.*

