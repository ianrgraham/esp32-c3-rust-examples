# ESP32-C3 Rust Examples

## Official Documentation

Please always prefer the official documentation to the instructions I have here. I was able to successfully compile and flash these examples from an x86 linux PC, but your milage may vary.

- [esp-rs](https://github.com/esp-rs)
- [The Rust on ESP Book](https://esp-rs.github.io/book/introduction.html)

## Installation

The ESP32-C3 chip contains a single RISC-V core, making it relatively straightforward to setup the Rust toolchain once you have [rustup](https://rustup.rs) installed. Run the following to setup the requirements for `no_std` binaries.

```
rustup toolchain install nightly --component rust-src
rustup target add riscv32imc-unknown-none-elf
```

And we will require the following for `std` binaries.

```
cargo install ldproxy
```

More thorough documentation can be found [here](https://esp-rs.github.io/book/installation/installation.html).

## Tools

To flash and monitor the outputs of programs we run on the ESP32-C3, we'll need the following crates.

```
cargo install cargo-espflash
cargo install cargo-espmonitor
```

## Examples

### RGB Rainbow

```
cd no-std/rgb
cargo espflash --release --monitor
```

## Other Resources

- [Ferrous Systems Training Examples](https://espressif-trainings.ferrous-systems.com/)