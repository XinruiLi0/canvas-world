This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started (Fresh clone)

Below are the minimal steps to run the frontend locally after cloning the repository.

1. Change into the frontend folder and install dependencies

```bash
cd frontend
# Install with your preferred package manager:
npm install
# or
pnpm install
# or
yarn install
```

2. Copy environment variables from the example (if provided) and fill in values

```bash
cp .env.example .env
# Edit .env and provide required values (API_KEYS, NEXT_PUBLIC_*, RPC URLs, etc.)
```

3. Start the development server

```bash
npm run dev
# or
pnpm dev
# Open http://localhost:3000
```

4. Common commands

```bash
# Build for production
npm run build

# Preview the production build locally
npm run start
```

## Notes

- Ensure your Node.js version meets the project requirement (often >= 16, check `package.json`).
- If you use pnpm or Yarn v2/berry, follow their docs for `.pnp` or workspace specific setup.
- The frontend may require contract addresses or RPC endpoints (set in `.env`) produced by `contracts` deployments.

## Learn More

Additional Next.js resources:

- [Next.js Documentation](https://nextjs.org/docs)
- [Learn Next.js](https://nextjs.org/learn)

