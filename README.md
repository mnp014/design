# EVM2 Design
> This repository contains documents describing the design and high-level overview of EVM 2.0. Expect the contents of this repository to be in flux: everything is still under discussion.

The goal for this repository is to track research and development of alternative VM's for use in Ethereum. Currently eWASM has had the most research.

## eWASM Design

eWASM is an experimental VM design for Ethereum that uses [WebAssembly](https://github.com/WebAssembly/design) as the [instruction set](https://en.wikipedia.org/wiki/Instruction_set). This design follows WebAssembly's [design](https://github.com/WebAssembly/design) which should be referenced for further details.

## What is Ethereum flavored WebAssembly (eWASM)?

> WebAssembly is a new, portable, size- and load-time-efficient format. WebAssembly is currently being designed as an open standard by a W3C Community Group.

Ethereum flavored WebAssembly or eWASM is a restricted subset of WASM to be used for contracts in Ethereum.

eWASM:
* specifies the semantics for an *eWASM contract*
* specifies an [Ethereum system module](https://github.com/ethereum/evm2.0-design/blob/master/eth_interface.md) to facilitate interaction with the Ethereum Environment from an *eWASM contract*.
* specifies [metering](https://github.com/ethereum/evm2.0-design/blob/master/metering.md) for instructions
* and aims to restrict [non-deterministic behavior](https://github.com/WebAssembly/design/blob/master/Nondeterminism.md)

### Glossary

* *eWASM contract*: a contract compiled to the eWASM specification
* *metering*: the act of measuring execution cost in a deterministic way

### Resources

* [Ethereum system module](./eth_interface.md)
* [Original Proposal](https://github.com/ethereum/EIPs/issues/48)
* [WASM's design docs](https://github.com/WebAssembly/design)
* [JS prototype](https://github.com/ethereumjs/ewasm-kernel)
* [JS metering prototype](https://github.com/wanderer/wasm-metering)

### Design Process & Contributing
For now, high-level design discussions should continue to be held in the design repository, via issues and pull requests. Feel free to file [issues](https://github.com/ethereum/ewasm-design/issues).

## Chat
[Gitter](https://gitter.im/ethereum/ewasm-design)
