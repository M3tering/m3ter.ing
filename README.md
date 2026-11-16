# m3ter.ing

The official landing page for **M3tering Protocol v2**, a smart contract protocol connecting real-world energy metering (such as solar) to onchain infrastructure on Ethereum.

🌐 **Live site:** [m3ter.ing](https://m3ter.ing/)
🏢 **Organization:** [@M3tering](https://github.com/M3tering)

---

## Overview

This repository contains the source for the public-facing website of M3tering v2. It introduces the protocol, explains what it does, and points visitors to the relevant resources, contracts, and community channels.

This is a standalone front-end project. It does not contain the protocol's smart contracts; those live in the [M3tering organization](https://github.com/M3tering).

## Tech Stack

| Layer                | Tool                                                        |
| -------------------- | ----------------------------------------------------------- |
| Framework            | [React Router v7](https://reactrouter.com/)                 |
| Language             | [TypeScript](https://www.typescriptlang.org/)               |
| Bundler / dev server | [Vite](https://vite.dev/)                                   |
| Styling              | [Tailwind CSS](https://tailwindcss.com/)                    |
| UI components        | [shadcn/ui](https://ui.shadcn.com/) (see `components.json`) |
| Package manager      | [Bun](https://bun.sh/)                                      |

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/) (recommended, since the repo ships a `bun.lock`)
- Alternatively, Node.js 20+ with npm

### Installation

```bash
git clone https://github.com/michaelchristwin/m3ter.ing.git
cd m3ter.ing
bun install
```

### Configuration

No environment variables are required. The project runs out of the box after installation.

### Development

Start the dev server with Hot Module Replacement:

```bash
bun run dev
```

The site will be available at [http://localhost:5173](http://localhost:5173).

### Production Build

```bash
bun run build
```

This generates the production output in `build/`:

```
build/
├── client/    # Static assets
└── server/    # Server-side code
```

To preview the production build locally:

```bash
bun run start
```

### Type Checking

```bash
bun run typecheck
```

> If you prefer npm, replace `bun install` with `npm install` and `bun run <script>` with `npm run <script>`.

## Project Structure

```
.
├── app/                     # Routes, components, and application code
├── public/                  # Static assets served as-is
├── components.json          # shadcn/ui configuration
├── react-router.config.ts   # React Router configuration
├── vite.config.ts           # Vite configuration
├── tsconfig.json            # TypeScript configuration
└── package.json
```

## Deployment

Deploy the output of `bun run build` (the `build/` directory along with `package.json` and your lockfile) to any platform that supports Node.js applications, such as Vercel, Netlify, Railway, Fly.io, or a VPS. Since there are no environment variables, no secrets or additional platform configuration are needed.

If your host serves static files only, check `react-router.config.ts` to confirm how rendering is configured before choosing a static hosting target.

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-change`
3. Commit your changes: `git commit -m "feat: describe your change"`
4. Push to your branch: `git push origin feat/your-change`
5. Open a pull request

For bugs or suggestions, please [open an issue](https://github.com/michaelchristwin/m3ter.ing/issues).

## Related

- [M3tering organization](https://github.com/M3tering): protocol repositories and contracts
- [m3ter.ing](https://m3ter.ing/): the live landing page

## License

No license has been specified yet. Add a `LICENSE` file to clarify how others may use this code.
