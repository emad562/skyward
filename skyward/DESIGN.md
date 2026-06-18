# Skyward — design doc (v1 scope lock)

*A solo, web-first 3D exploration platformer. Mario Odyssey's structure, Minecraft's
sky, none of the parts that sink solo projects.*

---

## The one feeling
**Wonder through movement.** The player should want to climb to the high place
*just to see it*, and feel good getting there. Everything below serves that. If a
feature doesn't make moving-and-looking better, it's cut.

## The pitch in one line
Wander handcrafted floating "kingdoms," gather sunshards, climb to vantage points,
and watch the day and weather turn around you.

---

## Core loop
See something interesting → figure out the route → enjoy the traversal → arrive,
collect, get a new sightline → repeat. That loop *is* the game. It must be fun in a
grey box before any art exists.

## Moveset (deliberately small)
- **Run** (camera-relative)
- **Sprint** (hold)
- **Jump → double-jump**
- **Air dash** (carries across gaps; short cooldown)

That's enough for expressive traversal without a Nintendo-sized animation budget.
No attacks. No stamina. No inventory. Add a move only if a whole kingdom needs it.

## Structure
Discrete **kingdoms** (Odyssey-style), not one seamless map. Each is a small,
dense, self-contained sandbox you can fully explore. **v1 ships with 1–2 kingdoms.**
Each new kingdom is its own milestone and its own releasable chunk.

## Atmosphere (the cheap wonder)
- **Day/night cycle** (~90s full day in the prototype; tune later)
- **Weather states:** clear / fog / rain
- Time and weather should *occasionally reveal something* — a path you notice at
  dusk, a sound only in fog. Atmosphere that's also a mechanic.

This layer is added **after** movement feels right, never before.

---

## Milestone order (each stage is releasable)
1. **Grey-box playground** — blocky platforms + the character controller, no art.
   *Gate: is hopping around the ugly box fun on its own? If no, stop and fix the
   controller. Nothing else proceeds.* ← the prototype you have now is this stage.
2. **One real kingdom** — verticality, sightlines, "get up there" moments, a handful
   of collectibles. Get the core loop singing in one space.
3. **Atmosphere** — day/night + weather over that one kingdom. Highest wonder-per-hour.
4. **Second kingdom** — only once the first is genuinely good. Self-contained.
5. **Ship** — 1–2 strong kingdoms, ~1 hour of play, on itch.io / GitHub Pages.

## NOT in v1 (where feature creep goes to die)
- Voxel building / terrain editing (you confirmed: free exploration *feeling* only)
- Combat, enemies, health
- NPCs with dialogue/voice
- Save system, settings menus, options (until the loop is proven fun)
- Procedural worlds (handcraft first; proc-gen is a later force multiplier, not a v1)
- Multiplayer, achievements, story cutscenes

## Tech
- **Three.js**, single-file, runs in any browser, hosted on **GitHub Pages** (free URL).
- Web-first because the goal is "open via a link." (Godot is a fine alt and also
  exports to web — switch only if you outgrow hand-rolling 3D in JS.)

## Honest risk
A 3D platformer lives on movement feel, which is the product of relentless iteration.
Target **"feels good and readable,"** not "Odyssey-tight." Chasing Nintendo's polish
is how a solo year disappears. Ship readable-and-fun; polish in patches.
