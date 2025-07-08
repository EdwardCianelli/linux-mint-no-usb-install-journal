# 🧯 Errors and Fixes

## Kernel Panic
- ✅ Fixed by switching from loopback ISO boot to extracted kernel/initrd files

## VFAT/VFS Errors
- Caused by booting ISO from FAT32 — fixed by loading Puppy to RAM

## Missing `filesystem.squashfs`
- Mint failed to find root filesystem when ISO was unpacked — fixed by avoiding `findiso=` and using full ISO instead

## GRUB Device Mismatch
- `(hd1,2)` sometimes became `(hd0,2)` depending on boot order — used `search --file` to dynamically find correct device
