# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A mailing email loop web app for a friend group to stay in touch, built as a Next.js app inside `my-app/`.

## Commands

All commands run from `my-app/`:

```bash
npm run dev      # Start dev server
npm run build    # Production build
npm run start    # Start production server
npm run lint     # Run ESLint
```

## Important: Next.js Version Warning

This project uses **Next.js 16.2.4** with **React 19**, which has breaking changes from older versions. APIs, conventions, and file structure may differ from training data. Before writing any Next.js code, read the relevant guide in:

```
my-app/node_modules/next/dist/docs/
```

Key subdirectories:
- `01-app/` — App Router docs (used by this project)
- `02-pages/` — Pages Router docs

## Architecture

- **Framework**: Next.js 16 with App Router (`src/app/`)
- **Styling**: Tailwind CSS v4 (configured via `postcss.config.mjs`)
- **Language**: TypeScript
- **Fonts**: Geist Sans + Geist Mono via `next/font/google`

The app uses the App Router layout convention:
- `src/app/layout.tsx` — root layout with font setup and global CSS
- `src/app/page.tsx` — home page (currently the default scaffold)
- `src/app/globals.css` — global styles

Route handlers (API routes) belong in `src/app/api/` per App Router convention — verify the exact API in `node_modules/next/dist/docs/01-app/01-getting-started/15-route-handlers.md` before implementing.
