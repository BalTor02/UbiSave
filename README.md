<div align="center">

  <img src="UbiSave_logo.png" alt="UbiSave Logo" width="180" />

  <br><br>

# UbiSave

**A Ubisoft Games Save Editor — quest and exploration completion, nothing else.**

> **Status:** 🚧 Concept reserved. Not yet in development.
> This repository exists to hold the name and document the plan. No code has been written yet.

---

## What UbiSave will be

UbiSave is a planned save editor for single-player Ubisoft titles, focused narrowly on **narrative and world-state completion** — the kind of thing you'd otherwise have to grind out by hand. It is not a general-purpose save editor, and it isn't trying to be.

## Scope

**In scope:**
- Mission / quest completion status
- Exploration / region completion percentage
- Other "did this happen" flags that fit the same category (collectibles found, codex/lore entries, discovery markers)

**Explicitly out of scope, permanently:**
- In-game currency
- Items, gear, stats, health, or any form of character power
- DLC content or unlocks
- Anything a game's real-money store also sells
- Multiplayer titles or titles protected by anti-cheat (EAC, BattlEye, etc.)
- Titles whose save data is wrapped in commercial anti-tamper protection (e.g. VMProtect) — these will be skipped, not reverse engineered

## Design principle

If a value has a price tag or makes a character stronger, UbiSave doesn't touch it. It edits *state* not *value*. That line is the whole design philosophy, and it's meant to be permanent, not a starting point that expands later.

## Known challenges (being researched before any code is written)

- Ubisoft's back catalog spans ~400 titles with inconsistent, undocumented save formats. This will require a per-title approach rather than one generic parser.
- Some completion fields double as achievement triggers in a given title. Flipping one could unintentionally fire an achievement unlock as a side effect, which runs against the whole point of keeping this tool clean. Every exposed field will need to be checked per-title before shipping, not assumed safe. That's where [UbiSlot](https://github.com/BalTor02/UbiSlot) comes in handy!
- Some titles chain additional world-state (NPC spawns, follow-up quest triggers) off completion flags. Editing a flag without accounting for what depends on it risks producing an inconsistent, broken save rather than a working one.

## Relation to UbiSlot

[UbiSlot](https://github.com/BalTor02/UbiSlot), a Ubisoft achievement browser and management tool. UbiSave is a separate project by design, not a feature bolted onto UbiSlot.

## License

TBD — will be added once development begins.

## Timeline

None yet. This project is paused indefinitely while other work takes priority. Watch/star if you want to know if and when that changes.
