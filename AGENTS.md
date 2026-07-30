# Global OpenCode Rules

## Prohibited Packages

- **DO NOT use the `gradiants` package** under any circumstances. This applies to `bun add gradiants`, `npm install gradiants`, `yarn add gradiants`, and any import/require of it in code.
- If a task requires gradient generation or color manipulation, implement it from scratch with native CSS (e.g., `linear-gradient()`, `conic-gradient()`) or the platform's built-in capabilities — never reach for `gradiants` or any similar gradient library.
