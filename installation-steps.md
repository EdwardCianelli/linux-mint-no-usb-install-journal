# 📜 Installation Steps

## Phase 1: Initial Setup
- Disabled Secure Boot in UEFI firmware
- Installed **Grub2Win** in Windows 11
- Downloaded **Linux Mint 22.1 Cinnamon ISO**
- Downloaded **Fossapup64 9.5 ISO**
- Created a `puppy` folder on second HDD (formatted as FAT32 initially)
- Extracted `vmlinuz`, `initrd.gz`, `.sfs` from Fossapup ISO into `/puppy`

## Phase 2: Booting Puppy via Grub2Win
```bash
search --no-floppy --set=root --file /puppy/initrd.gz
linux /puppy/vmlinuz pmedia=cd psubdir=puppy pfix=ram
initrd /puppy/initrd.gz
boot
```
- Puppy Linux booted entirely into RAM, leaving drives unmounted

## Phase 3: Format Target HDD
- Used `gparted` to format second HDD as **ext4**
- Moved Linux Mint ISO to `/mnt/sda1` (NTFS)

## Phase 4: Burn ISO to HDD with `dd`
```bash
dd if=/mnt/sda1/linuxmint-22.1-cinnamon-64bit.iso of=/dev/sdb bs=4M status=progress
sync
```
- Burned Mint ISO to second HDD using raw image write

## Phase 5: Boot Into Linux Mint
- Rebooted and used boot menu to select second HDD
- Linux Mint Live environment loaded successfully
- Installed Mint to second HDD using graphical installer
