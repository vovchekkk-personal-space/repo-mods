# Truck Slot Machine v1.0.2
Adds a working slot machine to the REPO truck with synced multiplayer spins, animated reels, configurable gamble costs, shop payouts that give money, and level payouts that give player upgrades. 
Grab the handle, pay the price, watch the reels spin for real, and let gambling ritual decide if you get paid, upgraded, or simply humbled.

![Shop Slots](https://i.ibb.co/J8wKC6p/Shop.gif)

![Level Slots](https://i.ibb.co/mrxwZRX0/Level.gif)

## Discord server

- http://discord.gg/empress

## What This Mod Does

- Adds a working slot machine to the truck.
- Spawns in shop and levels
- Syncs spins and results in multiplayer.
- Uses host-authoritative logic so every player sees the same result.
- Only pays out on full three-symbol matches.
- Supports REPOConfig so hosts can adjust gamble costs in-game.

## How It Works

Players interact with the slot machine by grabbing the handle.

That means:

- the player grabs the handle
- the reels spin for all players
- the result lands after the animation
- rewards are only given once the spin finishes and to the player who actually grabbed it (For upgrades)

## Shop Gambling

In shop scenes, the slot machine uses money.

| Result | Reward |
| --- | --- |
| `777` | Jackpot payout |
| Three matching non-7 symbols | Big payout |
| Mixed symbols | No payout |
| Two matching symbols | No payout |

Shop spins cost `1K` by default.

Hosts can set the shop spin cost to:

| Setting | Cost |
| --- | --- |
| `1` | `1K` |
| `10` | `10K` |
| `100` | `100K` |

## Level Gambling

In real levels, the slot machine uses health instead of money.

| Result | Reward |
| --- | --- |
| `777` | Random upgrade |
| Three matching non-7 symbols | Random upgrade |
| Mixed symbols | No reward |
| Two matching symbols | No reward |

Level spins cost `5` health by default.

Hosts can set the level spin health cost to:

| Setting | Health Cost |
| --- | --- |
| `5` | `5` health |
| `10` | `10` health |
| `50` | `50` health |
| `999` | `999` health |

## Config Settings

| Setting | Default | What it changes |
| --- | --- | --- |
| `Shop Spin Cost K` | `1` | Sets shop spin cost in thousands |
| `Level Spin Health Cost` | `5` | Sets health cost for real level spins |

## Notes

- This mod works in both singleplayer and multiplayer.
- Multiplayer spins are host-authoritative by design.
- Clients can use the slot machine, but the host decides the actual result.
- Rewards are applied after the spin animation finishes.
- The machine only pays on full matches.

## Credits

- Created by **Omniscye/Empress**

> The truck has a slot machine now. This is either an upgrade or a warning.