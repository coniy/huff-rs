<img align="right" width="150" height="150" top="100" src="./assets/huff.png">

# huff-rs • [![tests](https://github.com/huff-language/huff-rs/actions/workflows/tests.yaml/badge.svg)](https://github.com/huff-language/huff-rs/actions/workflows/tests.yaml) ![GitHub](https://img.shields.io/github/license/huff-language/huff-rs) ![Crates.io](https://img.shields.io/crates/v/huff-rs) ![Discord](https://img.shields.io/discord/980519274600882306)

> `huff-rs` is a [Huff](https://github.com/huff-language) compiler built in rust.


## What is a Huff?

Huff is a low-level programming language designed for developing highly optimized smart contracts that run on the Ethereum Virtual Machine (EVM). Huff does not hide the inner workings of the EVM. Instead, Huff exposes its programming stack to the developer for manual manipulation.

Rather than having functions, Huff has macros - individual blocks of bytecode that can be rigorously tested and evaluated using the Huff runtime testing suite.

[Huff](https://github.com/AztecProtocol/huff) was originally developed by the Aztec Protocol team to write [Weierstrudel](https://github.com/aztecprotocol/weierstrudel). Weierstrudel is an on-chain elliptical curve arithmetic library that requires incredibly optimized code that neither [Solidity](https://docs.soliditylang.org/en/v0.8.14/) nor [Yul](https://docs.soliditylang.org/en/v0.8.9/yul.html) could provide.

While EVM experts can use Huff to write highly-efficient smart contracts for use in production, it can also serve as a way for beginners to learn more about the EVM.

To dive deeper into [Huff](https://github.com/huff-language), visit the [Official Huff Docs](https://huff.sh)(also available on [github](https://github.com/huff-language/huff-docs)).


## Installation

_Something not working? Send a message in [discord](https://discord.gg/2uuJyatE6M)._

First run the command below to get `huffup`, the Huff installer:

```bash
curl -L https://huff.nascent.xyz | bash
```

To avoid redirecting the script directly into bash, download and run the [huffup installation script](https://raw.githubusercontent.com/huff-language/huff-rs/main/huffup/huffup).

To install the Huff compiler, simply run `huffup`.

**Alternatively**

Install from source by running:

```bash
git clone https://raw.githubusercontent.com/huff-language/huff-rs
cd huff-rs
cargo install --path ./huff_cli --bins --locked --force
```

OR

```bash
cargo install --git https://raw.githubusercontent.com/huff-language/huff-rs --locked huff_cli
```


## How Fast?

**Compilation Benchmarks**

| Compiler                         | Cold (No Cache) | Light Cache | Deep Cache | Full Cache |
| -------------------------------- | --------------- | ----------- | ---------- | ---------- |
| [huff-language/huff-rs][huff-rs] |           XXXms |       XXXms |      XXXms |      XXXms |
| [huff-language/huffc][huffc]     |           XXXms |       XXXms |      XXXms |      XXXms |

_Note: Compilation benchmarks were performed on [huff-examples erc20](https://github.com/huff-language/huff-examples/tree/main/erc20/contracts/ERC20.huff)._


## Contributing

All contributions are welcome! We want to make contributing to this project as easy and transparent as possible, whether it's:
  - Reporting a bug
  - Discussing the current state of the code
  - Submitting a fix
  - Proposing new features
  - Becoming a maintainer

We use GitHub issues to track public bugs. Report a bug by [opening a new issue](https://github.com/huff-language/huff-rs/issues/new); it's that easy!

To pass github actions, please run:

```bash
cargo check --all
cargo test --all --all-features
cargo +nightly fmt -- --check
cargo +nightly clippy --all --all-features -- -D warnings
```

In order to fix any formatting issues, run:

```bash
cargo +nightly fmt --all
```

**Recommended PR Template**

Here is an example PR template - not strictly required, but will greatly improve the speed at which your PR is reviewed & merged!

```md
## Overview

<Provide a general overview of what your pr accomplishes, why, and how (including links)>

## Checklist

- [x] <Ex: Added a `new` method to the Huff Lexer [here](./huff_lexer/src/lib.rs#50)>
- [x] <Ex: Fully tested the `new` method [here](./huff_lexer/tests/new.rs)>
- [ ] <Ex: Wrote documentation for the `new` method [here](./huff_lexer/README.md#20)>
```

When the PR checklist isn't complete, it is **highly** recommended to make it a draft PR. NOTE: if your PR is not complete, it will likely be changed to a draft by one of the repository admins.


## Acknowledgements

The original [Huff Language](https://github.com/huff-language) compiler: [`huffc`](https://github.com/huff-language/huffc).

An exemplary, minimal rust compiler: [ripc](https://github.com/ibraheemdev/ripc).

[Foundry](https://github.com/foundry-rs/foundry), for the many scripts, documentation, devops, and code on which [huff-rs](https://github.com/huff-language/huff-rs) is based on.

All [huff-rs](https://github.com/huff-language/huff-rs) contributors, users, advocates, and discord enthusiasts!
