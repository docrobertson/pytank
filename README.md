# pytank

Combat tank!

A 3D tank target-practice game inspired by Atari 2600 *Combat*. It runs in the browser on desktop and mobile, with a chase camera behind and above your tank.

## Play

Open `index.html` in a browser through any static web server, for example:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

To play on your phone, turn on GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch) and open the Pages URL. On iPhone, Share → Add to Home Screen runs it full screen.

The page loads three.js from the jsDelivr CDN, so the first load needs an internet connection.

## How it works

- **Practice mode:** destroy every target in the wave before the clock hits zero. Leftover seconds turn into bonus points.
- **Waves ramp up:** more targets, less time per target, and a faster tank and soundtrack each wave. Drones show up at wave 3, enemy tanks at wave 4, and from wave 5 the tanks shoot back. A hit spins you out Combat-style and costs 3 seconds.
- **Shells ricochet once.** A bank shot is worth 50% more, and the aim line shows the bounce.
- **Red barrels explode** and chain through anything nearby.
- **Combos:** kills within 2.5 seconds of each other multiply points, up to x8. Clearing a wave from 5 onward without taking a hit pays a no-hit bonus.
- **Heavy handling:** the tank builds up speed, coasts to a stop and winds into and out of turns. The hull rocks on its suspension, and walls stop you with a thud.
- **Aim assist:** a shot locks onto a target just off your aim line (the line turns orange) and leads moving targets. It's a little stronger on touch screens.
- **Guide arrow:** once three or fewer targets are left, an arrow by your tank points to the nearest one.
- **Pickups:** Rapid Fire, Spread Shot and +5 seconds. A rainbow bonus target appears mid-wave and is worth +5 seconds.

## Controls

| | Desktop | Touch |
|---|---|---|
| Drive / turn | W A S D or arrow keys | Left thumb anywhere on the left half (the stick follows your thumb) |
| Fire | Space (hold for auto-fire) | Hold anywhere on the right half |
| Pause | P or Esc | II button |
| Sound | M (music + FX → FX only → off) | ♪ button |

Gamepads work too: left stick or d-pad to drive, A or a trigger to fire, Start to pause.

Your best score is saved in the browser.
