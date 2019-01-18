Cross compile NixOS to Aarch64
---

# Building for Raspberry Pi 3

```bash
$ nix build -I nixpkgs=https://github.com/Mic92/nixpkgs/archive/raspberry-cross-fixes.tar.gz -f ./system.nix config.system.build.sdImage -o sdImage
$ sudo dd if=sdImage/sd-image/*.img of=/dev/YOUR_SD_CARD status=progress
```
