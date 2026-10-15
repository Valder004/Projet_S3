# Projet S3

Astro + Tailwind CSS v4 + PocketBase, géré avec Bun.

## Installation

```bash
bun install
cp .env.example .env
```

## Lancer le projet (2 terminaux)

```bash
bun run db    # PocketBase  → http://127.0.0.1:8091/_/
bun run dev   # Astro       → http://localhost:4321
```

Au premier lancement de PocketBase, ouvrir le lien affiché dans le terminal pour créer le compte superuser.

## Structure

```
pocketbase/            binaire PocketBase (pocketbase.exe, non versionné) + pb_migrations/
src/lib/pocketbase.ts  client PocketBase partagé
src/layouts/           layout principal (importe Tailwind)
src/pages/             pages Astro
src/styles/global.css  @import "tailwindcss"
```

Le binaire PocketBase n'est pas versionné : le télécharger sur
https://github.com/pocketbase/pocketbase/releases et le placer dans `pocketbase/`.
