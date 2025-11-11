
## Foundry

**Foundry is a fast, modular Ethereum development toolkit implemented in Rust.**

Main components:

- **Forge**: Testing and building toolkit (similar to Hardhat or Truffle).
- **Cast**: CLI tool for interacting with the EVM and contracts.
- **Anvil**: Local EVM node (similar to Ganache or Hardhat Network).
- **Chisel**: A Solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Getting Started (Fresh clone)

Follow these steps after cloning the repository on a machine that doesn't yet have Foundry installed.

1. Install Foundry (if not already present):

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

2. Prepare project dependencies

```bash
cd contracts
# If the repository does not vendor the `lib/` directory, install external libraries:
forge install
# If you manage dependencies via git submodules instead, run:
git submodule update --init --recursive
```

3. Build and run tests

```bash
forge build
forge test
```

4. Common commands

```bash
# Format code
forge fmt

# Start a local node
anvil

# Create gas snapshot
forge snapshot

# Example: run a deploy script with an RPC and private key
forge script script/Counter.s.sol:CounterScript --rpc-url <RPC_URL> --private-key <PRIVATE_KEY>

# Use cast for ad-hoc interactions
cast <subcommand>

# Help
forge --help
anvil --help
cast --help
```

## Notes

- The `lib/` folder normally contains external libraries (for example `forge-std`). If you want a true "out-of-the-box" experience, commit `lib/` into the repo; otherwise require developers/CI to run `forge install` or `git submodule` to fetch dependencies.
- `.env` files often store secrets (RPC URLs, private keys) and should be ignored by version control. Provide a `.env.example` as a template instead.

