# GitHub export package — Game Development Studio

Generated 2026-11-25 for the `game-development-studio` branch of
[znex07/gundamtwitterbot](https://github.com/znex07/gundamtwitterbot/tree/game-development-studio)
(the browser extension on `main` stays untouched).

Contents of this folder:

- `README.md` — the studio README (features, built-in scenes, repo layout). Same file the studio's Export tab downloads.
- `studio.json` — the studio manifest: stack, modes, renderers, shading styles, scene list, and app source file paths.
- `scenes.json` — every built-in scene as editable entity JSON, generated from the studio's own scene builders: Voxel Dog — Tiny Voxel (390 entities), Voxel Desk — Dog at Work (399), Ghibli Meadow (34), Tiny Dog — Super Deformed (30), Dog Character 3D (20), Platformer Meadow 2D (10), Neon Orbit 3D (7) — 890 entities total. The bundled dog artwork is referenced by its repo path (`client/src/assets/pig-character.jpg`).

The studio itself (Export tab, or the "Full package" button by Export JSON) downloads the complete bundle as
`game-development-studio-source-package.json`, which additionally includes the user's saved projects and the
current scene at the moment of export — those live in the app database, so they are exported from the running
studio rather than from this folder.
