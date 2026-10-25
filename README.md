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

- **Mazes and the uplink:** each level is a generated maze with an entrance and an exit gate. Stand in the blue uplink zone to charge the gate; holding it draws raiders, so it plays like a short last stand. Power cores are optional: each one keeps spawning enemies, and destroying it charges the uplink by 35%. Wipe out every enemy and the gate opens on its own; either way the uplink collapses once it's no longer needed. Every fifth maze is a boss fight instead. Clearing a maze quickly pays bonus experience, and every orb left on the map flies to you when the exit opens.
- **Enemies:** crawlers rush you, gunner tanks fire aimed fans, sentries fire rings, spinners spray spirals, heavies lob shells that burst. Gold elites have triple armour and drop triple experience plus a pickup.
- **Your health:** hearts in the HUD; a bar over your tank (armour charges in cyan) pops up for a few seconds whenever they change. A damaged tank smokes, and at one heart the screen edges glow red.
- **Bullet hell rules:** your hitbox is much smaller than your tank. Near misses ("grazes") pay a little experience. Dashing makes you briefly untouchable and rams crawlers.
- **Kill streaks:** kills less than two seconds apart build a streak that multiplies experience, up to x1.6.
- **Level-up cards:** pick one of three. You get a reroll per maze cleared (up to 3 banked). Cards show what you have now and what you'll have after.
- **Skills** are simple steps, most with no cap: Autoloader (+10% fire rate), Heavy Shells (+10% damage), Long Barrel (shell speed and range), Engine Tune (speed), Salvager (experience), Tractor Beam (pickup range), Nitro (dash recharge), Field Repair (heart regeneration) and Battering Ram (dashes damage what they plow through). Gun Sight (crits) caps at 100% and Hull Plating at 10 hearts.
- **Gear** changes how you fight and fills one of three slots (a fourth comes from the first boss). Each piece upgrades to level 3: Multi-Cannon, Ricochet Rounds, Seeker Shells, Piercing Rounds, Flak Shells, Reactive Armor, Escort Drones and EMP Pulse (wipes nearby shots, hurts and shoves enemies). Gear on a timer shows a cooldown sweep in its slot.
- **Pickups:** icon cubes in dead ends and from cores are permanent: each adds a skill rank or repairs a heart. From maze 2 a blue supply crate hides in the deepest dead end with a choice of gear; bosses drop a gold crate.
- **Seeing your build:** gear sits in the slots under your hearts and skills show as a row of icons with ranks on wider screens. Pause to see the full loadout with what each piece does right now.

## Controls

| | Desktop | Touch |
|---|---|---|
| Drive | W A S D or arrow keys | Put a thumb down (left half in Arcade); the stick appears under it and stays put |
| Arcade: fire | Space (hold for auto-fire) | Hold anywhere on the right half |
| Rogue: dash | Space or Shift | Tap a second finger, or the Dash button |
| Rogue: pick a card | 1, 2, 3 or click (R rerolls) | Tap |
| Pause | P or Esc | II button |
| Sound | M (music + FX → FX only → off) | ♪ button |

Gamepads work too: left stick or d-pad to drive, A or a trigger to fire (Arcade) or dash (Rogue), Start to pause.

Your best Arcade score and deepest Rogue maze are saved in the browser.
