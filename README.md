# Listoxi 🛒

**Listoxi** is a modern, collaborative shopping and task list application designed with an **offline-first** architecture and real-time synchronization.

Built with **Svelte 5** (Runes), **SvelteKit 2**, **Dexie.js** for local in-browser persistence, and **PocketBase** as the authentication and synchronization backend.

---

## ✨ Key Features

- 📴 **Offline-First Architecture**: Work seamlessly without an internet connection. Data is stored locally via IndexedDB with [Dexie.js](https://dexie.com/).
- 🔄 **Bidirectional Synchronization**: Automatic synchronization and conflict resolution with [PocketBase](https://pocketbase.io/) as soon as network connectivity is restored.
- 👥 **Shared Lists**: Share shopping lists and collaborate with other users via email invitations.
- 🎨 **Modern Interface & WebAwesome**: Clean, accessible UI components powered by `@awesome.me/webawesome`.
- 🌓 **Dark / Light Mode**: Integrated support for toggling visual themes.
- 🏷️ **Emoji Customization**: Personalize and quickly recognize lists using custom emoji tags.
- 📦 **PWA / Service Worker**: Configured for rapid, reliable progressive web app installation across mobile and desktop devices.

---

## 🛠️ Tech Stack

- **Frontend:** [Svelte 5](https://svelte.dev/) (using modern Runes: `$state`, `$derived`, `$effect`, `$props`)
- **Meta-framework:** [SvelteKit 2](https://kit.svelte.dev/) configured with `@sveltejs/adapter-static`
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Local Database (Offline):** [Dexie.js](https://dexie.com/) (IndexedDB)
- **Backend & Auth:** [PocketBase](https://pocketbase.io/)
- **Component Library:** [WebAwesome](https://webawesome.com/) (`@awesome.me/webawesome`)
- **Bundler:** [Vite](https://vite.dev/)
- **Package Manager:** [pnpm](https://pnpm.io/)
- **Containerization:** Docker & Docker Compose (Nginx + PocketBase)

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v20+ recommended)
- **pnpm** (recommended via Corepack: `corepack enable && corepack prepare pnpm@latest --activate`)
- A running **PocketBase** instance (local or remote)

### 1. Clone the Repository

```bash
git clone https://github.com/esaramago/listoxi.git
cd listoxi
```

### 2. Install Dependencies

```bash
pnpm install
```

### 3. Configure Environment Variables

Copy `.env.example` to create `.env`:

```bash
cp .env.example .env
```

Edit `.env` as required:

```env
# URL of your PocketBase instance (e.g. https://pb.listoxi.com or http://localhost:8090)
PUBLIC_POCKETBASE_URL=http://localhost:8090
ENV=development
```

### 4. Run the Development Server

```bash
pnpm run dev
```

The application will be available at `http://localhost:5173`.

---

## 📄 License

This repository is private and/or governed by the terms specified by the repository owner.
