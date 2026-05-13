# Wigum Gaming

Wigum Gaming is the company-level workspace for planning, documentation, images, business material, store material, and long-term direction that does not belong directly inside a specific game or website repository.

This folder is for the shared structure around the studio, not for active game source code. Individual games and the public website stay in their own repositories.

## Purpose

Use this workspace for:

- Company planning and roadmap documents.
- Studio identity, brand notes, and reusable images.
- Release planning, store-page drafts, and marketing material.
- Cross-project decisions that affect more than one game.
- Notes about workflows, standards, and lessons learned from each project.

Do not use this folder for:

- Godot project source code.
- Website application code.
- Blog posts or public website content that should live in `BloggStorage`.
- Temporary scripts or personal shell commands.

## Connected Repositories

The current Wigum Gaming workspace is split across these project areas:

- `https://github.com/OL3s/MobArena`: first priority game, currently the main active project.
- `https://github.com/OL3s/MultiplayerArenaV2`: multiplayer arena project with an early systems foundation.
- `https://github.com/OL3s/SinglePlayerRogueliteV2`: roguelite project with an early systems foundation.
- `https://github.com/OL3s/WigumGamingWebpage`: public homepage.
- `https://github.com/OL3s/Blogg-Storage`: public content storage for game metadata, about-us content, images, and dev blog posts.

## Studio Direction

Wigum Gaming is focused on accessible games built around shared experiences, cross-device support, controller compatibility, and lightweight Godot-based development.

The current strategy is to build strong foundations through smaller 2D projects before expanding into larger or more complex games. Each project should teach systems, workflows, and design patterns that can improve the next one.

## Current Focus

The current main focus is `Mob Gladiator`, developed in the `MobArena` repository.

The first goal is to finish a small, structured, playable prototype before pushing the other projects further. The experience from that project should help shape future work on Multiplayer Arena and especially the roguelite project.

See `ROADMAP.md` for the staged project order.

## Folder Structure

The company workspace uses this top-level structure:

```text
WigumGaming/
  README.md
  ROADMAP.md
  FOCUSPOINT.md
  brand/
  business/
  images/
```

Folder use:

- `brand/`: studio identity, naming, tone, logos, colors, and shared visual direction.
- `business/`: company planning, release strategy, store drafts, pricing notes, infrastructure, and business decisions.
- `images/`: shared company-level images that do not belong to one specific game repository.
- `FOCUSPOINT.md`: what to focus on next after the current work session.

Current business notes:

- `business/hosting-and-domain.md`: website hosting and domain provider notes.
