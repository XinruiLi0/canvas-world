# Canvas World

This repository contains a full-stack Web3 starter project with smart contracts (Foundry) and a frontend (Next.js).

Project layout (top-level folders):

- `contracts/` — Foundry Solidity contracts, tests, scripts and dependencies (usually the `lib/` folder).
- `frontend/` — Next.js application for the UI.

## Quick start (fresh clone)

Follow these minimal steps after cloning the repository to get both contract and frontend development environments running locally.

1) Clone the repository and enter it

```bash
git clone <your-repo-url> canvas-world
cd canvas-world
```

2) Contracts (Foundry)

Install Foundry if you don't have it yet:

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

Prepare dependencies and build/test the contracts:

```bash
cd contracts
# If the repo does not vendor `lib/`, install external libraries
forge install
# If dependencies are managed via git submodules:
git submodule update --init --recursive

# Build and run tests
forge build
forge test
```

3) Frontend (Next.js)

```bash
cd ../frontend
# Install dependencies (choose one)
npm install
# or
pnpm install
# or
yarn install

# Copy env template if provided and fill values
cp .env.example .env

# Start development server
npm run dev
# Open http://localhost:3000
```

4) Environment variables and secrets

Environment files such as `.env` often contain secrets (RPC URLs, private keys) and should not be committed. Use `.env.example` as a template and copy it to `.env` locally.

For more detailed instructions, see `contracts/README.md` and `frontend/README.md`.
