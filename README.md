# linux-concepts

A deconstructed guide to Linux fundamentals. Documentation for the layman and the persistent learner.

## 📂 Project Structure & Navigation

To maintain a professional and organized learning environment, this repository follows a modular structure. Use the guide below to navigate the technical deep-dives and monthly progress logs.

```text
linux-concepts/
├── scripts/             # Automation tools (e.g., generate_release.sh)
├── modules/             # Technical deep-dives categorized by topic
│   ├── 01-linux-boot-and-init/   # BIOS/UEFI → GRUB → Kernel Init → Systemd (PID 1)
├── releases/            # Monthly "Astronomical" learning logs
│   └── v1.0.0-mercury/  # Milestone-specific reflections
├── RELEASES.md          # Monthly roadmap and index
└── README.md            # Mission, Navigation and Index
```

## 📖 Technical Modules

Explore the deconstructed concepts by category. These modules break down the complex inner workings of Linux into smaller, achievable tasks.

* **./modules/**
  * 📂 [**01-Linux-Boot-and-Init**](./modules/01-linux-boot-and-init/) — Deconstructing the journey from hardware power-on to a usable shell.
    * **Focus:** BIOS/UEFI, GRUB, Kernel Initialization, and the role of Systemd (PID 1).
