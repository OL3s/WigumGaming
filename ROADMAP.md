# Wigum Gaming Roadmap

This roadmap describes the current staged direction for Wigum Gaming projects. It is company-level planning, not a replacement for the detailed task lists inside each game repository.

## High-Level Order

1. Mob Gladiator
2. Multiplayer Arena
3. Roguelite Project
4. Choose the next path

The current stage is `1. Mob Gladiator`.

Projects 2 and 3 already have early foundations, but they are not the main production focus yet. They should benefit from the systems, structure, and lessons learned while building the first game.

## 1. Mob Gladiator

Repository: `https://github.com/OL3s/MobArena`

Status: active main focus.

Mob Gladiator is the first priority because it is a focused 2D project with a clear loop: manage a gladiator company, prepare fighters, enter arena contracts, survive combat, earn rewards, and return to town.

Primary goals:

- Build the first complete small playable loop.
- Establish practical Godot C# project structure.
- Develop reusable patterns for scenes, overlays, save/runtime data, UI, and input.
- Support phone, controller, and desktop interaction from the beginning.
- Keep the first version scoped around one small prototype before expanding systems.

Expected learning value:

- Company/player data structure.
- Runtime save-state patterns.
- Management UI and overlays.
- Combat prototype structure.
- Touch/controller/desktop menu handling.
- Practical release discipline for a small game.

## 2. Multiplayer Arena

Repository: `https://github.com/OL3s/MultiplayerArenaV2`

Status: early foundation exists.

Multiplayer Arena is a fast 2D PvP arena shooter built around movement, aiming, items, networking, and destructible arenas.

The project already has important early systems: LAN testing, destructible map logic, shared damage concepts, player item/action tests, and multiplayer setup work.

This project should continue after Mob Gladiator has produced enough stable patterns to reuse.

Expected reuse from Mob Gladiator:

- Cleaner scene organization.
- Better reusable UI components.
- Improved input patterns across keyboard, controller, and touch.
- Stronger save/config/runtime data separation.
- More disciplined prototype-to-MVP planning.

Main future challenge:

- Multiplayer authority, sync, split-screen identity, item validation, and readable arena combat.

## 3. Roguelite Project

Repository: `https://github.com/OL3s/SinglePlayerRogueliteV2`

Status: early foundation exists.

The roguelite project is planned around repeated runs, path choices, upgrades, bosses, and collecting three gems across multiple attempts.

This project should especially benefit from Mob Gladiator because both games need progression, items, save data, UI-heavy flows, character state, and between-run preparation.

Expected reuse from Mob Gladiator:

- Outpost/town-style management patterns.
- Character and roster-style data structures.
- Item, equipment, and reward flow lessons.
- Save/autoload patterns.
- Mobile-first UI decisions.
- Clearer milestone planning before expanding content.

Main future challenge:

- Turning the early menu/outpost/item foundation into a full run-based loop with combat, path choice, bosses, rewards, and long-term progression.

## 4. Choose The Next Path

After the first three project stages are clearer, Wigum Gaming should choose the next direction based on what has been learned and what is most realistic to finish.

Possible paths:

- Continue polishing one of the three projects toward public release.
- Start a smaller experimental project to test a missing system.
- Expand into stylized low-poly 3D after the 2D foundation is stronger.
- Build shared tooling, templates, or pipelines for future Godot projects.
- Rework the public website and store presence around the strongest project.

The next path should be chosen based on finished prototypes, not only ideas.

## Guiding Principle

Finish small, useful foundations before building large systems.

Every project should leave behind reusable structure, better workflows, and clearer decisions for the next one.
