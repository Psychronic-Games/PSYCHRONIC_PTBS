# PSYCHRONIC_PTBS

**RPG Maker MZ Plugin**

Psychronic Tactical Battle System (PTBS) with Win Condition Editor

## What It Does

Psychronic Tactical Battle System (PTBS) with Win Condition Editor.

## Plugin File

- `PSYCHRONIC_PTBS.js`
- Version: `1.0.4`
- Target: RPG Maker MZ
- Author: Psychronic
- URL: https://psychronic.itch.io

## Plugin Commands

- `PTBS_StartBattle`
- `PTBS_RecoverBattlers`
- `setWinConditions`
- `PTBS_SetCursorPosition`
- `PTBS_SetCursorToEvent`
- `PTBS_ReleaseCameraLock`
- `PTBS_HideUI`
- `PTBS_ShowUI`

## Parameter Summary

- BlockedRegions: List of region IDs that block battler movement in PTBS battles. Separate with commas (e.g., 1, 2, 3).
- FrontDamageMultiplier: Damage multiplier when attacking a battler from the front.
- SideDamageMultiplier: Damage multiplier when attacking a battler from the side.
- BackDamageMultiplier: Damage multiplier when attacking a battler from the back.
- switchId: Which switch to check
- state: Required switch state (ON = true, OFF = false)
- variableId: Which variable to check
- operator
- value: Target value for variable comparison
- count: Number of turns that must pass
- {object} params - projectile config from <PTBS_Projectile> note
- {object} startPos - {x, y} in map-coordinates
- {object} targetPos - {x, y} in map-coordinates
- {function} onComplete - callback after it lands

## Installation

1. Download `PSYCHRONIC_PTBS.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.
