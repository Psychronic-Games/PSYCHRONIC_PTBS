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

### Start PTBS Battle

- Command: `PTBS_StartBattle`
- Description: Starts a tactical battle, pausing the current event.

Arguments:

- `victorySwitch` (Victory Switch (Global)) - type: switch; default: 0: The global switch to turn ON upon winning the battle. 0 for none.
- `victorySelfSwitch` (Victory Self-Switch) - type: select; default: ""; options: None, A, B, C, D: The self-switch (A, B, C, or D) to turn ON upon winning.
- `victorySelfSwitchEventId` (Victory Self-Switch Event ID) - type: number; default: 1: The ID of the event to which the victory self-switch belongs.
- `defeatSwitch` (Defeat Switch (Global)) - type: switch; default: 0: The global switch to turn ON upon losing the battle.  0 for none.
- `defeatSelfSwitch` (Defeat Self-Switch) - type: select; default: ""; options: None, A, B, C, D: The self-switch (A, B, C, or D) to turn ON upon losing.
- `defeatSelfSwitchEventId` (Defeat Self-Switch Event ID) - type: number; default: 1: The ID of the event to which the defeat self-switch belongs.

### Recover PTBS Battlers

- Command: `PTBS_RecoverBattlers`
- Description: Restore HP/MP and/or remove states for certain battlers (ally, enemy, neutral, etc.)

Arguments:

- `faction` (Faction to Recover) - type: select; default: all; options: All Factions, Allies Only, Enemies Only, Neutral Faction: Which faction’s battlers to recover?
- `recoverHp` (Recover HP) - type: boolean; default: true: If ON, fully heal HP for the selected faction's battlers.
- `recoverMp` (Recover MP) - type: boolean; default: true: If ON, fully restore MP for actors in the selected faction.
- `removeStates` (Remove Negative States) - type: boolean; default: false: If ON, remove negative or KO states from the selected faction's battlers.

### Set Win Conditions

- Command: `setWinConditions`
- Description: Adds multiple victory conditions to this battle.

Arguments:

- `conditions` (Win Conditions List) - type: select[]; default: []; options: {"type":"defeatEnemies"}, {"type":"switch","switchId":1,"switchState":true}, {"type":"variable","variableId":1,"comparison":"==","value":0}, {"type":"turns","turnCount":1}: A list of win conditions. Battle ends when ANY condition is met.

### Set Cursor Position

- Command: `PTBS_SetCursorPosition`
- Description: Moves the PTBS cursor to a specific X,Y position on the map.

Arguments:

- `x` (X Coordinate) - type: number; default: 0: X coordinate to move the cursor to
- `y` (Y Coordinate) - type: number; default: 0: Y coordinate to move the cursor to
- `centerCamera` (Center Camera) - type: boolean; default: true: If true, centers the camera on the cursor position

### Set Cursor To Event

- Command: `PTBS_SetCursorToEvent`
- Description: Moves the PTBS cursor to a specific event's position.

Arguments:

- `eventId` (Event ID) - type: number; default: 1: ID of the event to move the cursor to
- `centerCamera` (Center Camera) - type: boolean; default: true: If true, centers the camera on the event
- `centerSpeed` (Camera Movement Speed) - default: 4: How fast the camera moves to center (1 = slow, 10 = fast)

### PTBS_ReleaseCameraLock

- Command: `PTBS_ReleaseCameraLock`
- Description: Releases any camera lock established by the SetCursorToEvent command.

### Hide PTBS UI

- Command: `PTBS_HideUI`
- Description: Hides all PTBS battle UI elements during a battle.

### Show PTBS UI

- Command: `PTBS_ShowUI`
- Description: Shows all PTBS battle UI elements during a battle.

## Parameter Summary

- BlockedRegions: List of region IDs that block battler movement in PTBS battles. Separate with commas (e.g., 1, 2, 3).
- FrontDamageMultiplier: Damage multiplier when attacking a battler from the front.
- SideDamageMultiplier: Damage multiplier when attacking a battler from the side.
- BackDamageMultiplier: Shows all PTBS battle UI elements during a battle.

## Installation

1. Download `PSYCHRONIC_PTBS.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.
