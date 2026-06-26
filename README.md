# coolinator-wrath
Coolinator-Wrath is a Wrath 3.3.5 cooldown and combat-awareness addon featuring cooldown tracking, smart proc detection, execute alerts, hotbar highlighting, keybind overlays, equipment cooldown tracking, profiles, and freeform layouts. Created specifically for Wrath clients.

# Coolinator-Wrath

Coolinator-Wrath began as a Wrath 3.3.5 backport of the Retail Coolinator addon. Over time it has evolved into a complete cooldown, proc, execute, and combat-awareness system built specifically for Wrath clients.

## Highlights

### Cooldown Tracking

* Spell cooldowns
* Item cooldowns
* Aura tracking
* Ready notifications
* Cooldown timers

### Smart Proc Engine

Supports Wrath talent and proc interactions across all classes.

Examples:

* Art of War → Exorcism
* Infusion of Light → Holy Light / Flash of Light
* Hot Streak → Pyroblast
* Rime → Howling Blast
* Lock and Load → Explosive Shot
* Maelstrom Weapon → Instant casts
* Eclipse → Starfire / Wrath
* Nightfall → Shadow Bolt

### Execute Detection

Automatic execute-phase awareness:

* Hammer of Wrath
* Execute
* Kill Shot

### Alert Layers

PROC, BUFF, and EXECUTE alerts with separate colors and behaviors.

### Hotbar Integration

Highlights action bar buttons directly, including macro support.

### Keybind Overlays

Displays keybinds on alerts when available.

Example:

USE EXORCISM [R]

EXECUTE HAMMER OF WRATH [4]

### Equipment Cooldown Tracking

Track:

* Trinket 1
* Trinket 2
* Gloves

without tracking specific item IDs.

### Popout Alerts

Center-screen combat alerts with priority handling and anti-spam protection.

### Profiles

* Character Profiles
* Spec Profiles
* Import / Export

### Freeform Layout System

Drag-and-drop icon placement with persistent saved positions.

**Coolinator-Wrath v1.2.4 — Smart Proc Audit Update**

This update builds on the v1.2.0 Combat Awareness release with major cleanup to hotbar handling, proc filtering, and smart-proc recommendation behavior.

Added
Added per-proc filtering so players can disable specific smart procs without turning off the entire smart proc system.
Added new proc filter commands:
/cw procignore <proc name>
/cw procallow <proc name>
/cw proctoggle <proc name>
/cw procignored

Added /cw procaudit support command for reviewing mapped proc behavior.

Added Proc Filters controls to the options window.

Proc filter settings are now saved and included with profiles.

Changed

Smart proc recommendations are now more conservative for broad utility buffs.

Broad buffs no longer force center-screen recommendations when the addon cannot safely determine a single best action.

Clearcasting now uses class-aware handling instead of a mixed all-class spell list.

Omen of Clarity now behaves like Clearcasting and no longer defaults to Regrowth as a generic recommendation.

Elemental Focus and other Clearcasting-style effects are now handled more safely.

Presence of Mind, Arcane Potency, Nature’s Grace, Borrowed Time, and Eradication no longer force center-screen recommendations.

Passive or non-actionable buffs such as Ancestral Awakening, Holy Concentration, and Improved Spirit Tap are ignored by default.

Hotbar highlighting can still appear for relevant supported spells when a proc is active.

Fixed

Fixed stale hotbar USE / EXECUTE overlays after switching specs or action bar layouts.

Fixed duplicate ElvUI/private-client clone buttons lighting up at the same time.

Removed broad frame scanning from the hotbar resolver to prevent false action-button matches.

Fixed Clearcasting incorrectly recommending Regrowth for users where that was not an appropriate primary action.

Fixed proc recommendation spam from broad shared buff categories.

Improved smart proc behavior across hybrid classes and private-client action bar setups.

Notes

This release focuses on making the smart proc system less noisy and more accurate. Coolinator-Wrath should now do a better job distinguishing between true “press this now” procs and broader buffs that are useful but should not always create a forced recommendation.


