# Global OpenCode Rules

## Prohibited Packages

- **DO NOT use the `gradiants` package** under any circumstances. This applies to `bun add gradiants`, `npm install gradiants`, `yarn add gradiants`, and any import/require of it in code.
- If a task requires gradient generation or color manipulation, implement it from scratch with native CSS (e.g., `linear-gradient()`, `conic-gradient()`) or the platform's built-in capabilities — never reach for `gradiants` or any similar gradient library.

## STE Writing (always active)

Write prose in ASD-STE100 Simplified Technical English. This applies to documentation, READMEs, pull-request text, error messages, release notes, and comments. It does not apply to code, identifiers, or command syntax.

**Rules:** Active voice. One name for one thing. Short common words (use, not utilize; start, not initiate). No marketing adjectives. One instruction per sentence. Max 20 words per sentence (instructional) / 25 (descriptive).