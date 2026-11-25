# Game Development Studio

A browser game-development studio with 2D and 3D modes in one editor, built with React + three.js.
Projects are saved server-side (Bun actions + Drizzle/SQLite) and every scene is made of editable entities.

## Features

- 2D and 3D editors with drag-to-move entities, orbit/pan/zoom camera, and a turntable mode
- WebGL and WebGPU render backends (three.js WebGPURenderer, with WebGL fallback) plus a live WebGPU compute-shader test (WGSL, x² + 10)
- Play mode with per-entity behaviors: spin, bounce (gravity), float, orbit, pulse, drift, patrol
- Standard and Ghibli shading — Ghibli mode is banded toon shading (MeshToonMaterial, 4-step gradient map) after craftzdog's ghibli-style-shader
- Frosted-glass UI after craftz.dog: translucent backdrop-blur panels, warm charcoal / cream themes, teal + pink accents
- Import your own image as a textured plane, export/import scenes as JSON, save / duplicate / delete projects
- GitHub export (Export tab): downloads a full source package — README, studio.json manifest, every built-in scene as entity JSON, the current scene, and all saved projects

## Built-in scenes

- Voxel Dog — Tiny Voxel
- Tiny Dog — Super Deformed
- Dog Character 3D
- Voxel Desk — Dog at Work
- Ghibli Meadow
- Neon Orbit 3D
- Platformer Meadow 2D

The dog character is a dog (light tan fur, pale yellow hoodie, light tan backpack, brown pants and boots, black nose with a cream XX button). The voxel version is built from matte cube voxels on a 0.16-unit grid with a stepped panel head and a round belly.

## Repository layout (app source)

- `client/src/App.tsx` — Studio UI, WebGL/WebGPU viewport (three.js), Play mode, and every built-in scene
- `client/src/api.ts` — Typed client for the server actions
- `client/src/theme.css` — Frosted-glass theme — dark charcoal / cream, teal + pink accents
- `client/src/assets/pig-character.jpg` — Bundled dog character artwork, used as the in-scene reference texture
- `server/src/actions.ts` — Project actions: list, get, save, delete, duplicate
- `server/src/schema.ts` — Projects table (Drizzle ORM / SQLite)
- `drizzle/` — SQL migrations for the projects table
- `package.json` — Dependencies: react, three, drizzle-orm, @hatch/space-sdk, tailwindcss
- `space.json` — Artifact metadata — name, slug, runtime

## This branch

Pushed to the `game-development-studio` branch of znex07/gundamtwitterbot so the browser extension on `main` (manifest.json, popup.html, popup.js, images/) stays untouched.

Style references: https://www.craftz.dog · https://github.com/craftzdog/ghibli-style-shader · https://github.com/craftzdog/
