# Skyward (prototype)

A web-based 3D exploration platformer prototype — Three.js, single file, no build step.
This is **milestone 1**: the grey-box "is moving around fun?" test. See `DESIGN.md`
for the full scope.

## Run it locally
Just open `index.html` in a browser. (No server needed — it loads Three.js from a CDN.)

## Put it online with GitHub Pages (free URL)
1. Create a new repo on GitHub, e.g. `skyward`.
2. Add `index.html` (and `DESIGN.md`, `README.md`) to the repo root and push.
3. Repo **Settings → Pages → Build and deployment**.
4. Source: **Deploy from a branch**. Branch: **main**, folder: **/ (root)**. Save.
5. Wait ~1 minute. Your game is live at:
   `https://<your-username>.github.io/skyward/`

Because the file is named `index.html` and sits at the repo root, that URL loads the
game directly — the "open via a link" you wanted. Every push updates the live site.

## Controls
- **WASD** move · **Shift** sprint
- **Space** jump / double-jump · **F** air dash
- **drag mouse** or **← →** look · **wheel** zoom · **R** cycle weather

Goal: gather all 12 sunshards. Some sit on floating islands that need a double-jump +
dash to reach. No way to lose — fall off and you respawn.

## What's in here / what's faked
- Real: camera-relative movement, double-jump, air dash, AABB collision, third-person
  follow cam, 12 collectibles, day/night cycle (~90s), three weather states.
- Grey-box on purpose: placeholder geometry and colors, one "kingdom," no audio, no menus.

## I couldn't playtest this
It was written and **syntax-checked**, and the movement math was reasoned through, but
I can't run a browser here — so I haven't *watched* it move. Open it and tell me what's
off and I'll fix it. Likely first things to tune: jump height/gravity feel, camera
follow speed, dash distance, whether sprint feels right. Those are all one-number tweaks.

## Next step (from DESIGN.md)
If hopping around this grey box is already a little bit fun, the foundation holds and
the next milestone is turning one area into a real kingdom — *then* art and audio.
If it's *not* fun yet, we fix the controller before anything else. That's the whole
point of shipping this stage first.
