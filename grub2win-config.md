# ⚙ Grub2Win Boot Configurations

## Puppy Linux (Extracted):
```bash
search --no-floppy --set=root --file /puppy/initrd.gz
linux /puppy/vmlinuz pmedia=cd psubdir=puppy pfix=ram
initrd /puppy/initrd.gz
boot
```

## Linux Mint (Extracted ISO — NOT WORKING):
```bash
search --no-floppy --set=root --file /mint/casper/filesystem.squashfs
linux /mint/casper/vmlinuz boot=casper noeject quiet splash toram live-media-path=/mint/casper/
initrd /mint/casper/initrd.lz
boot
```
> ⚠️ This failed due to missing full ISO. Mint's `casper` expects loopback or USB-like structure.
