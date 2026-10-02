# CLAUDE.md

This repo is a small React project that readers clone to follow a blog tutorial. Treat the code as teaching material: someone will read every line alongside a blog post.

## Principles

- Prefer plain, direct code over abstraction. Keep files and functions small.
- Build only what was asked for. No speculative features, options, or helpers.
- Comment the why when it isn't obvious. Don't narrate what the code does.

## Tooling

- Use npm only, on Node 24 (see `.nvmrc`). Never add Bun, pnpm, or Yarn files.
- Ask before adding any dependency.
- Before calling work done, run `npm run lint`, `npm run format:check`, `npm test`, and `npm run build`. Fix anything they report.

## Components

- Function components, one per file, in `src/components/`.
- Name the file after the component in PascalCase: `ChatInput.tsx` exports `ChatInput`.
- Use named exports, not default exports.
- Declare props as `type ChatInputProps = { ... }` above the component. Don't use `React.FC`.
- Use React's built-in hooks for state. Add a state library only if the tutorial is about it.

## Styling

- Global styles (resets, fonts, theme variables) go in `src/index.css`.
- Component styles go in a CSS Module next to the component: `ChatInput.module.css`, imported as `styles`.

## Tests

- Vitest. Put tests next to the code they cover as `*.test.ts` or `*.test.tsx`.
- Import test functions explicitly: `import { expect, test } from 'vitest';`.
- Component rendering tests need `jsdom` and `@testing-library/react`, which aren't installed. Ask before adding them.

## Environment variables

- List each variable in `.env.example` and declare its type in `src/vite-env.d.ts` as `string | undefined`.
- `VITE_` variables are bundled into browser code. They are fine for local tutorials but never safe for a secret in a deployed app.
