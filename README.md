# Auto Child Education (1.1.10)

Stop-gap update of [Auto Child Education](https://steamcommunity.com/sharedfiles/filedetails/?id=3607293096) by [victoriaposting](https://steamcommunity.com/id/victoriaposting) for EU5 1.1.x compatibility.

All credit to victoriaposting for the original mod.

## How It Works

Every month, all children with revealed traits (age 3+) are evaluated by calculating their base aptitude modifiers (subtracting current education bonuses) and assigned to the education type matching their highest base modifier.

Examples:
- Intelligent child (base adm +0.5) -> Administrative education
- Gregarious child (base dip +0.5) -> Diplomatic education
- Rowdy child (base mil +0.5) -> Military education
- Ambitious child (base adm +0.33, dip +0.33) -> Administrative education (tie-break)
- Gallant child (base dip +0.33, mil +0.33) -> Diplomatic education (tie-break)
- Shrewd child (base mil +0.33, adm +0.33) -> Administrative education (tie-break)
- Prodigy, gifted, slow, idiot -> Rotates through ADM, DIP, MIL

## Settings

Open any child's education selection screen to find the Auto Education panel:

- **Exclude Heirs** - skip heirs so you can manage them manually
- **Exclude Crown Estate** - skip crown estate children
- **Exclude Prodigy/Gifted** - skip prodigies and gifted (they cap stats regardless)
- **Expensive Education** - automatically assign expensive in-depth education to heirs and crown estate children (250 gold + 1% court spending per child)
- **Run Now** - immediately re-process all eligible children

## v2.4 Changes

- **Expensive Education toggle**: auto-assign expensive education to heirs and crown estate children (off by default)
- **Fixed trait detection**: children with prodigy, gifted, slow, or idiot traits were never being processed due to a modifier check bug
- **Performance**: AI countries short-circuited at on_action level instead of inside the effect block
- **Restored is_child**: Paradox re-added the trigger in 1.1.10
- **Debug event**: `event ace_debug.1` spawns test children of your ruler

## Links

- Workshop (this fork): https://steamcommunity.com/sharedfiles/filedetails/?id=3681510822
- Workshop (original): https://steamcommunity.com/sharedfiles/filedetails/?id=3607293096
- GitHub (original): https://github.com/victoria-riley-barnett/autoChildEducation
