# Changelog
## [0.2.4] - Shop and Sync Fixes
- Fixed DHH items and upgrades being added to the game after the latest update.
- Improved multiplayer sync when using DHH upgrades.
- Reworked the shop settings for DHH items.
- Added a fallback for a ScalerCore + DHH Last Chance camera issue where the DHH spectate FOV could get stuck at 0.

## [0.2.3] - DHH Integration Cleanup
- Removed the extra secret shop section and disabled several obsolete systems from the original DHH mod.
- DHH Head Charge items and upgrades now join the normal pool, with config options to control how often they can appear.
- Improved Charge audio handling, including a multiplayer loop fix for the looping sound that could get stuck after use.
- Cleaned up and simplified older code paths for better stability.

## [0.2.2] - Game Update 0.4.0
- Compatibility fix for game version 0.4.0. Some minor issues may still be present and will be checked later

## [0.2.1] - Updated Readme
- Updated Readme

## [0.2.0] - Fix Singleplayer
- Fixed jump and all the behaviours of the mod in Singleplayer mode

## [0.1.9] - Photon + Head Charger sync
- Synchronizes a dedicated `DHHPunManager` PhotonView ID through `DhhPunViewIdRoomKey` so RPCs stop failing or misaligning during shelf updates.
- Ensures the shop/prefab registry caches every alias/normalized asset name it encounters, which brings the `HeadCharger` battery back to the attic without skipping it.
- Keeps charge ability state checks tied to `DHHStatsManager.GetHeadChargeUpgrade` so clients reflect the real head charge slot state even after master/client swaps.
- Added "hold"" to charge ability to calibrate the direction/power. Now it fires when the button is released.

## [0.1.8] - Fixes
- Ensure JumpBattery checks honor the `BatteryJumpEnabled` flag so the player head can still jump when the battery system is intentionally disabled.
- Prevented the head from jumping infinitely without draining battery energy after holding jump, so the energy meter now ticks down per hop.
- Fixes on Bepinex variables management

## [0.1.7] - Sound and Host JumpBattery fix
- Trying to stop the looping sound after using the charge ability
- Added a guard to prevent a dead player’s jump from consuming the host’s death battery

## [0.1.6] - Debug logging improvements
- Debug logging Jump and Ability.

## [0.1.5] - Jump tuning
- Change default jump curve and fix upgrade effectiveness.

## [0.1.4] - Debug logging
- Added Debug gate to Deferred Audio log.

## [0.1.2] - Shop tuning
- Added `ShopItemsSpawnChance` as a second-tier gate so each selected Shelf slot may still fail to produce an item, giving 0–5 DHH upgrades per run depending on two separate probabilities.

## [0.1.1] - Bug Fixes
- Fixes PhysGrabber.ReleaseObjectRPC(bool, float) called by DeathHeadHopper with incorrect parameters.

## [0.1.0] - First public release
- Initial public release introducing every compatibility and stability patch for DeathHeadHopper 2.1.8 plus some customizations :)

