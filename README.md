# Svelte Catch Bug Reproducer
This repo contains a reproducer for a svelte bug that crashes the vite dev server entirely.

See https://github.com/sveltejs/svelte/issues/10501

## Svelte versions
This can be reproduced with both Svelte `4.2.11` and `5.0.0-next.55`. The latter can be found on the `svelte-5` branch.

## Reproduction Steps
1. clone repo
2. `npm i && npm run dev`
3. navigate to http://localhost:5173/
4. application crashes (see vite console)
