<div align="right">
  <img src="https://img.shields.io/badge/Status-🟠_In_Progress-orange" alt="Status: In Progress">
</div>

# 📂 01: Linux Boot Process and init

---

### Read in Blog Format at avidflick.in

To read a simplified, browser-friendly version of this guide, check out the post on my blog
👉 [**Read: [Post Title] @ avidflick.in**](https://avidflick.in/your-blog-post-link)

---

> [!NOTE]
> **Unknown Terms?**
> If terms like **CMOS**, **ROM**, or **SPI** sound like a different language, I've deconstructed them for you here:
> 👉 [**CMOS**](./glossary/what-is-cmos.md)
> 👉 [**ROM / Flash ROM**](./glossary/what-is-ROM-or-Flash-ROM-chip.md)
> 👉 [**Reset Vector + SPI**](./glossary/reset-vector-SPI-bus.md)

### The Reset Vector

When a CPU receives power, it is hardwired to look at a specific memory address called the **Reset Vector** (usually `0xFFFFFFF0`).

* **The Mechanism:** This address is mapped directly to the BIOS chip.
* **The Jump:** The CPU "jumps" to this location and immediately begins executing the BIOS code stored on the motherboard.

---

### BIOS (Basic Input/Output System)

BIOS is the firmware stored on a small ROM chip on your motherboard/CMOS. It is the **Initial Program Load (IPL)** that wakes the computer up. Think of it as the "pre-installed" set of instructions that tells the CPU how to find its surroundings.

> **The "Layman" Analogy:** BIOS is like the alarm clock and the morning routine. Before you can start your "Work" (The OS), you first need to wake up, check if your limbs are working, and remember where you left your shoes.

---

### Why BIOS? (The Purpose)

Without BIOS, a CPU is essentially a powerful engine with no ignition switch. It serves three critical functions:

#### 1. POST (Power-On Self-Test)

It acts as a **Diagnostic Doctor**. It performs a rapid health check:

* Is the RAM seated?
* Is the GPU alive?
* Is the CPU overheating?
* **The Beep Codes:** If something fails, the BIOS communicates through "Beep Codes" (the Morse code of hardware failure).

#### 2. Hardware Abstraction

In the early days of computing, BIOS provided a standardized way for software to talk to hardware (keyboard, screen, disk) without the software needing to know the specific brand or model of those parts.

#### 3. The Bootstrapping (The "Lift")

This is the most critical part for Linux.

1. BIOS scans the hardware for a bootable disk.
2. It looks at the **first 512 bytes** of that disk—known as the **Master Boot Record (MBR)**.
3. It loads those 512 bytes into RAM and hands over full control to the code found there.

---

### 🔙 Navigation & Roadmap

* **Main Index:** [Return to Technical Modules List](../../README.md#-technical-modules)

---
*Created by **Venkata Jagan Chennu** — DevOps Engineer | Simplifying Tech.*
