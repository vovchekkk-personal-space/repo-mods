# Death Head Hopper Fix
This mod builds on the work of *Death Head Hopper* version **2.1.8** by Cronchy—it's not a full replacement but a compatibility and stability patch that hardens runtime checks, recalculates jump/hop forces and expose some options.

## Updates
- In case of an update, I suggest resetting the configuration to the default values.

## New functionality
- Adds the ability to tie jumps to the `DeathBattery` function so each jump consumes battery energy, effectively limiting hop/spike forces when the device is drained.
- Introduces the option to recharge stamina using the same baseline that the vanilla game uses, while bumping the ability cost from 40 to 60 to keep it in check.
- Exposes every balance variable in `BepInEx/config/AdrenSnyder.DeathHeadHopperFix.cfg`, covering logging flags, battery thresholds, stamina recharge rates, cost scalars, and multiplier tweaks so you can tune them.
- Changed/Tuned some behaviours

## Multiplayer
- Every player (host and clients) must have this mod, and the original, installed.

## Configuration
The configuration file `BepInEx/config/AdrenSnyder.DeathHeadHopperFix.cfg` exposes all of the logging, battery, cost, and multiplier options that this patch applies.

## Credits
Thanks to Cronchy for creating the original *Death Head Hopper* mod that inspired this compatibility fix.  
Original mod: https://thunderstore.io/c/repo/p/Cronchy/DeathHeadHopper/

## Feedback and support
You can provide feedback or report bugs on the "[R.E.P.O. Modding Server](https://discord.com/invite/r-e-p-o-modding-server-1344557689979670578)"
