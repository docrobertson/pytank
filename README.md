# pytank

Combat tank!

A 3D tank game inspired by Atari 2600 *Combat*, with two modes. It runs in the browser on desktop and mobile.

## Play

Open `index.html` in a browser through any static web server, for example:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

To play on your phone, turn on GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch) and open the Pages URL. On iPhone, Share → Add to Home Screen runs it full screen.

The page loads three.js from the jsDelivr CDN, so the first load needs an internet connection.

## Arcade

Chase camera behind and above your tank. Destroy every target in the wave before the clock hits zero; leftover seconds turn into bonus points.

- **Waves ramp up:** more targets, less time per target, and a faster tank and soundtrack each wave. Drones show up at wave 3, enemy tanks at wave 4, and from wave 5 the tanks shoot back. A hit spins you out Combat-style and costs 3 seconds.
- **Ramming:** drive into a crate at speed to crush it. Ramming a barrel sets it off.
- **Barrels explode** and chain through anything nearby. Being within 5 units of a blast counts as a hit.
- **Shells ricochet once.** A bank shot is worth 50% more, and the aim line shows the bounce.
- **Combos:** kills within 2.5 seconds of each other multiply points, up to x8. Clearing a wave from 5 onward without taking a hit pays a no-hit bonus.
- **Sharpshooter:** clear a wave using no more than 2 shots per target (the HUD shows `SHOTS 5/12`) and every shot under the limit pays 150. Firing freely costs nothing except this bonus.
- **Heavy handling:** the tank builds up speed, coasts to a stop and winds into and out of turns.
- **Aim assist:** a shot locks onto a target just off your aim line (the line turns orange) and leads moving targets.
- **Pickups:** Rapid Fire, Spread Shot and +5 seconds. A rainbow bonus target appears mid-wave and is worth +5 seconds.

## Bullet Rogue

A high, north-up camera so you can see shots coming from every side. Your turret aims and fires by itself; you drive, dodge and dash.

- **Mazes:** each level is a generated maze with an entrance and an exit gate. Destroy the power cores to open the exit. Cores keep spawning enemies until they go down. Every fifth maze is a boss fight.
- **Enemies:** crawlers rush you, gunner tanks fire aimed fans, sentries fire rings, spinners spray spirals, heavies lob shells that burst. The deeper you go, the thicker the bullet storm.
- **Bullet hell rules:** your hitbox is much smaller than your tank. Near misses ("grazes") pay a little experience. Dashing makes you briefly untouchable and rams crawlers.
- **Experience and levels:** enemies drop experience orbs. Each level offers three cards.
- **Skills** are stackable numbers: Autoloader (fire rate), Heavy Shells (damage), Engine Tune (speed), Long Barrel (shell speed and range), Gun Sight (critical hits), Salvager (more experience), Tractor Beam (pickup range), Hull Plating (max hearts), Nitro (dash recharge) and Field Repair (heart regeneration).
- **Gear** changes how you fight and fills one of three slots (a fourth unlocks from the first boss). Each piece upgrades to level 3: Multi-Cannon, Ricochet Rounds, Seeker Shells, Piercing Rounds, Flak Shells, Reactive Armor, Escort Drones and EMP Pulse (wipes nearby shots).
- **Pickups:** letter cubes in dead ends and from cores are permanent: each one adds a skill rank or repairs a heart. Bosses drop a gear crate.

## Controls

| | Desktop | Touch |
|---|---|---|
| Drive | W A S D or arrow keys | Put a thumb down (left half in Arcade); the stick appears under it and stays put |
| Arcade: fire | Space (hold for auto-fire) | Hold anywhere on the right half |
| Rogue: dash | Space or Shift | Tap a second finger, or the Dash button |
| Rogue: pick a card | 1, 2, 3 or click | Tap |
| Pause | P or Esc | II button |
| Sound | M (music + FX → FX only → off) | ♪ button |

Gamepads work too: left stick or d-pad to drive, A or a trigger to fire (Arcade) or dash (Rogue), Start to pause.

Your best Arcade score and deepest Rogue maze are saved in the browser.
