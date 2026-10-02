# labs-[project-name]

[One sentence on what this project does and what it demonstrates.]

[Demo video or screenshot]

Tutorial: [link to the blog post]

## What it covers

- [Concept or technique 1]
- [Concept or technique 2]

## Setup

Requires Node 24 or newer.

```bash
npm install
cp .env.example .env.local
```

Add your API key to `.env.local`, then:

```bash
npm run dev
```

## Scripts

| Command                | What it does                                |
| ---------------------- | ------------------------------------------- |
| `npm run dev`          | Start the dev server                        |
| `npm run build`        | Type-check and build for production         |
| `npm run preview`      | Serve the production build locally          |
| `npm test`             | Run Vitest (watch mode locally, once in CI) |
| `npm run lint`         | Run ESLint                                  |
| `npm run format`       | Format with Prettier                        |
| `npm run format:check` | Check formatting without writing changes    |

## Starting a new lab from this template

Delete this section in the new repo.

1. Click "Use this template" on GitHub and name the repo `labs-[project-name]`.
2. Update `name` in `package.json` and the `<title>` in `index.html`.
3. Update the year in `LICENSE`.
4. Fill in the placeholders at the top of this README.

## License

MIT
