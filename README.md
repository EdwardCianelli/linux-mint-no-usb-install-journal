# Installing Linux Mint Cinnamon Without a USB Drive

This repository documents my successful attempt to install **Linux Mint Cinnamon 22.1** on my dual-drive laptop **without using a USB stick**. I completed this using **Grub2Win**, **Puppy Linux (Fossapup64 9.5)**, and a series of manually crafted GRUB2 configurations.

The process required resilience, deep Linux bootloader knowledge, filesystem understanding, and direct command-line work — all relevant to real-world cybersecurity work.

---

## 🔧 Tools and Environment

- **Laptop**: Acer Nitro AN515-53
- **Primary OS**: Windows 11 (initially)
- **Target OS**: Linux Mint Cinnamon 22.1
- **Second HDD**: Used to install Linux (no USB boot)
- **Grub2Win**: Bootloader GUI to add custom GRUB entries from Windows
- **Puppy Linux (Fossapup64 9.5)**: Temporary live OS used to burn ISO
- **Utilities**: `dd`, `gparted`, `lsblk`, `mount`, GRUB console

---

## 📁 Key Files

- [`installation-steps.md`](installation-steps.md) – all the steps I took
- [`grub2win-config.md`](grub2win-config.md) – my working GRUB entries
- [`errors-and-fixes.md`](errors-and-fixes.md) – what went wrong and how I fixed it
- [`lessons-for-security-analysts.md`](lessons-for-security-analysts.md) – what I learned that applies to real-world security

---

## 🧠 Why This Matters

Installing Linux without a USB required deep knowledge of:
- Bootloaders (GRUB2)
- Kernel/initrd handling
- Filesystems (ext4, vfat, squashfs)
- Manual troubleshooting

This is the kind of low-level skill that’s directly applicable to real-world cybersecurity work — especially in forensics, threat hunting, and malware reverse engineering.
