# Proposed Content Outline

This doc tracks an outline of pages to be written.

Please do not merge this page into the actual specs repo.
This is only filed as a pull request to allow folks to submit review comments

## Outline

### core

Contains concepts shared between layers.

`/core/serial`: Serialization of Rust typed structs

`/core/serial/bincode`: The bincode Rust serialization scheme
  (used in consensus, p2p)

`/core/tx`: Transaction and instruction format

### runtime

Specifies components required for chain replay.

`/runtime/sbf`: Solana Bytecode Format

`/runtime/sbf/elf`: Subset of ELF and loading/validation routine

`/runtime/sbf/isa`: Instruction Set and bytecode static verification routine

`/runtime/sbf/abi`: Solana bytecode in-memory ABI

`/runtime/sbf/syscalls`: Builtin VM syscalls

`/runtime/builtin`: Built-in runtime programs

`/runtime/builtin/...`: Pseudocode of built-in programs (system, vote, sigverify, ...)

`/runtime/sysvar`: Account sysvars

`/runtime/sysvar/...`: Composition of account sysvars (clok, fees, rent, epoch schedule, ...)

`/runtime/bank`: Bank hash

`/runtime/poh`: PoH hash chain

### consensus

Documents components involved in full validation.

`/consensus/block`: Solana block format (entries) and block validation rules

`/consensus/shred`: Solana shred format and FEC

`/consensus/tower-bft`: Tower BFT consensus protocol

### p2p

Defines network protocols required to drive aforementioned layers.

`/p2p/gossip`: Solana gossip and CRDS

`/p2p/tpu`: TPU/QUIC and TPU/UDP

`/p2p/turbine`: Turbine block propagation strategy

`/p2p/replay`: Replay request/reply protocol
