# Pocket Planet · Build a Little World
Original Vue + Canvas ecosystem game by John Parker. A rotating spherical world with 36 editable surface patches, forests, connected rivers, bunnies and rocks. Three guided missions use 18 building seeds; free build has no seed limit. Live ecosystem readings explain water, food and habitat shortages. Undo/redo, orbit controls, named local saves and a recoverable reset are included.

Node 22+: `npm ci`, `npm run dev`, `npm test`, `npm run build`. Vercel: Vite, dist output.

Drag to rotate and tap a visible patch to build. Keyboard: focus the planet; left/right orbit, up/down select patches, Enter or Space builds, 1–5 choose tools. Every action is also available through native HTML controls and a precise 36-tile selector. Touch uses Pointer Events and pointer capture. Sound starts only after its toggle. Reduced-motion suppresses automatic rotation and animal hopping. Saves validate data and tolerate unavailable storage.

The renderer uses Fibonacci sphere positions, depth sorting, front-face hit testing and Canvas 2D projection. It works without WebGL. Forests use one water; bunnies use two. Rivers supply three. Two forests provide one animal home and forests also supply food. These intentionally simple fictional rules explain cause and effect; they are not scientific ecosystem or climate predictions.

Original generated painted space backdrop; deterministic interactive planet, rivers, trees and creatures rendered in code.

## Full-window cosmos update
The former `planet-view` scenery is now a fixed, viewport-filling background behind the whole experience. The planet canvas remains transparent, with the name, orbit controls, life-support readings, mission card and building tools layered over the same continuous illustrated cosmos. Translucent panels preserve text contrast on desktop, tablet and phone; scrolling keeps every control accessible. Existing world storage, touch/keyboard controls and undo/redo are preserved.
