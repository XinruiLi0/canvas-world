
```markdown
# Canvas World

This repository contains a full-stack Web3 starter project with smart contracts (Foundry) and a frontend (Next.js).

Project layout (top-level folders):

- `contracts/` — Foundry Solidity contracts, tests, scripts and dependencies (usually the `lib/` folder).
- `frontend/` — Next.js application for the UI.

Quick start (fresh clone)

1) Clone the repository:

```bash
git clone <your-repo-url> canvas-world
cd canvas-world
```

2) Prepare and run the contracts (Foundry)

Install Foundry if you don't have it yet:

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

Enter the `contracts` folder and fetch dependencies if `lib/` is not vendored:

```bash
cd contracts
# Install external libraries referenced by the project
forge install
# If dependencies are managed as git submodules instead, run:
# git submodule update --init --recursive

# Build and test
forge build
forge test
```

3) Start the frontend (Next.js)

```bash
cd ../frontend
# Install dependencies with your package manager of choice
npm install
# or
pnpm install
# Start development server
npm run dev
# Open http://localhost:3000 in the browser
```

4) Environment variables / secrets

Environment files like `.env` often contain secrets and should not be committed. If the repo provides a template, copy it and fill values:

```bash
cp .env.example .env
```

For more details see `contracts/README.md` and `frontend/README.md`.

```
