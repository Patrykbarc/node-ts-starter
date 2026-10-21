# node-ts-starter

A template for new Node.js and TypeScript projects. TypeScript, the linter, the formatter, git hooks and VS Code are already configured, so you don't have to set them up from scratch every time.

## What's inside

- TypeScript 7 in `strict` mode, ESM modules (`nodenext`), source in `src/`, build output in `dist/`
- tsx for running code in watch mode
- oxlint as the linter and oxfmt as the formatter
- husky and lint-staged: lint and format changed files before each commit, run typecheck, lint and a format check before each push
- VS Code settings: format on save through the Oxc extension

## Libraries

All of them are dev dependencies.

| Package       | Version  | Used for                            |
| ------------- | -------- | ----------------------------------- |
| `typescript`  | ^7.0.2   | type checking and the build (`tsc`) |
| `@types/node` | ^24.19.2 | Node.js type definitions            |
| `tsx`         | ^4.23.15 | running TypeScript in dev mode      |
| `oxlint`      | ^1.89.0  | linting                             |
| `oxfmt`       | ^0.74.0  | formatting                          |
| `husky`       | ^9.1.7   | git hooks                           |
| `lint-staged` | ^17.6.0  | running tools only on staged files  |

## Start a new project

```sh
gh repo create my-project --template Patrykbarc/node-ts-starter --private --clone
cd my-project
pnpm install
```

Without creating a GitHub repo: `pnpm dlx degit Patrykbarc/node-ts-starter my-project`.

After copying, change `name` in `package.json`.

## Commands

| Command                             | What it does                        |
| ----------------------------------- | ----------------------------------- |
| `pnpm dev`                          | runs `src/index.ts` in watch mode   |
| `pnpm build`                        | compiles to `dist/`                 |
| `pnpm start`                        | runs `dist/index.js`                |
| `pnpm typecheck`                    | checks types without emitting files |
| `pnpm lint` / `pnpm lint:fix`       | oxlint, optionally applying fixes   |
| `pnpm format` / `pnpm format:check` | oxfmt, formats or only checks       |
