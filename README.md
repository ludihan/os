# lunaris

## Building
1. Enter the development shell using Nix (with flakes and new cli enabled):
```sh
nix develop
```

If you're not using nix/nixos you will need to install
[rustup](https://rustup.rs/), [QEMU](https://www.qemu.org/) and
[bootimage](https://github.com/rust-osdev/bootimage).

Both qemu and bootimage need to be in PATH.

2. Build and run the kernel inside QEMU:
```sh
cargo r
```

## TODO
- add UEFI support

## Useful resources:
- https://os.phil-opp.com/
- https://wiki.osdev.org/
