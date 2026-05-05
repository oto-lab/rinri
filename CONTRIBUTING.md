# Contributing to rinri

Thanks for your interest in contributing to the **技術者倫理を守ろう** site.

## Before you start

- File bugs and feature requests in [Issues](https://github.com/EdamAme-x/rinri/issues).
- For non-trivial changes, please open an issue first to discuss the design.
- Read the [Code of Conduct](./CODE_OF_CONDUCT.md). All contributors must follow it.

## Prerequisites

- Node.js **20+**
- pnpm **9+**

```bash
pnpm install
pnpm dev
```

## Branches and commits

- Branch naming: `feat/xxx`, `fix/xxx`, `docs/xxx`, `chore/xxx`
- Commit messages must follow [Conventional Commits](https://www.conventionalcommits.org/).
  - `feat: add X share button`
  - `fix(ogp): correct og:image URL`
  - `docs: clarify deploy steps`

## Checks before opening a PR

```bash
pnpm run type-check
pnpm run lint
pnpm run format:check
pnpm run build
```

All of the above must pass locally before requesting review.

## Pull request flow

1. Fork the repository and create a feature branch.
2. Make your changes with clear, atomic commits.
3. Open a PR against `main`.
4. Fill in the PR template.
5. Make sure CI is green.
6. Address review feedback, then a maintainer will merge.

## A note on ethics

In line with the theme of this site, please do not contribute changes that
conflict with engineering ethics. Be kind, be honest, ship responsibly.
