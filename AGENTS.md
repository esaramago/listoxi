# Project Rules

## Tech Stack

- **Framework:** Svelte 5 (use Runes: `$state`, `$derived`, `$effect`, `$props`, etc. instead of Svelte 4 reactive syntax).
- **Application Framework:** SvelteKit 2 (configured with `@sveltejs/adapter-static`).
- **Local Database (Offline):** Dexie.js (`src/lib/db.ts`).
- **Backend / Sync:** PocketBase (`src/lib/pb.ts` and sync in `src/lib/sync.ts`).
- **Component Library:** WebAwesome (`@awesome.me/webawesome`).
- **Language:** TypeScript (properly type everything).

## Useful Commands (always use `pnpm`)

- **Development:** `pnpm run dev`
- **Type/Svelte Check:** `pnpm run check`
- **Linters:** `pnpm run lint`
- **Formatting:** `pnpm run format`

## Guidelines for the Agent

1. **Validation:** After any code modification, always run `pnpm run format` and then `pnpm run check` / `pnpm run lint` to ensure code is clean, formatted, and error-free.
2. **Svelte 5 Runes:** Ensure new `.svelte` files use Runes and not legacy Svelte 4 syntax.
3. **Persistence / Sync:** Keep local synchronization with Dexie.js and remote synchronization with PocketBase in mind when handling data.

## Other Rules

- Code comments must be in English.
- App interface must be in Portuguese.
