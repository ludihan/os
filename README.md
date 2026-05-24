# lunaris

OS made in rust

## Setup

[bootimage]: https://github.com/rust-osdev/bootimage
[QEMU]: https://www.qemu.org/
[rustup]: https://rustup.rs/

### Nix/NixOS (using flakes and new cli)

Enter the devShell by running:
```
nix develop
```

### Other systems

Install [rustup], [QEMU] and [bootimage], ensure they are in PATH

## Building

You can build the project by running:

```
cargo build # or "cargo b"
```

Build a bootable disk image by running:

```
cargo bootimage
```

This creates a bootable disk image in the `target/x86_64-lunaris/debug` directory.

## Running

You can run the disk image in [QEMU] through:

```
cargo run # or "cargo r"
```

You can also write the image to an USB stick for booting it on a real machine. On Linux, the command for this is:

```
dd if=target/x86_64-lunaris/debug/bootimage-lunaris.bin of=/dev/sdX && sync
```

Where `sdX` is the device name of your USB stick. **Be careful** to choose the correct device name, because everything on that device is overwritten.

## Testing

To run the unit and integration tests by running:

```
cargo test # or "cargo t"
```

## TODO

- add UEFI support (possibly use newer versions of bootloader crate)
- add shell
- add graphical user interface
- add programs

## Useful resources:

- https://os.phil-opp.com/
- https://wiki.osdev.org/
