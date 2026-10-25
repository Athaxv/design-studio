# DESIGN.md — Winter Ice-Fishing Lake Diorama (`sloemo01/diorama`)

## 1. Premise
A square cutout of a snow-rimmed frozen alpine lake where a bundled winter angler casts into a dark ice hole, hooks a leaping silver-teal trout in a burst of droplets, and hands the catch to a camp scout arriving along the snowy bank.

## 2. Camera Side
- **Rig**: Locked three-quarter orthographic-feel perspective (`fov: 20.5°`, `azimuth: 45°`, `elevation: 33°`, `target: (0, -0.15, 0)`).
- **Front (`+x, +z`)**: Low snow banks and the open frozen ice sheet (`11.2m × 11.2m` slab) keep the sightline to the circular ice hole `(0.3, -0.6)` completely unobstructed.
- **Center-Right (`+x, -z`)**: The angler sits on a cedar folding stool at `(1.35, -1.15)` facing the ice hole, flanked by an oak catch bucket and a red enamel thermos.
- **Back (`-x, -z` & `+x, -z` rims)**: Layered snow-laden spruce trees and bare winter birch clusters frame the back-left `(-3.8, -3.4)` and back-right `(3.6, -3.2)` corners without crossing the central lake sightline.

## 3. Cast Sheet
1. **Finn (Lead Angler)**:
   - **Outfit**: Forest-green puffy winter parka (`#2f5b3a`), charcoal knit beanie with pom (`#23262b`), warm cream scarf (`#e6dfd3`), dark slate snow trousers (`#2d333b`), russet boots.
   - **Home**: Seated on wooden stool at `(1.35, 0.02, -1.15)`, facing `-2.35 rad` toward the ice hole `(0.2, -0.45)`.
   - **Action**: Casts the cedar rod (`Beat 1`), leans forward as the bobber dips (`Beat 2`), rears back in a two-handed reel-in as the trout leaps (`Beat 3`), pivots to hold up the catch toward Maya (`Beat 4`), and takes a warm sip from the red thermos (`Beat 5`).
2. **Maya (Camp Scout & Spotter)**:
   - **Outfit**: Vermilion-rust insulated parka (`#c84b31`), navy wool beanie (`#24344d`), ochre scarf (`#d99b26`), slate pants (`#343b46`).
   - **Home / Path**: Patrols the snowy north-west bank from `(-3.1, 0.28, 1.4)` to `(-1.25, 0.08, -0.65)`.
   - **Action**: Walks down the snowy bank carrying a brass camp lantern (`Beat 1`), pauses and points at the dipping bobber (`Beat 2`), cheers with raised arms as the fish breaches (`Beat 3`), kneels by the oak bucket to inspect the catch (`Beat 4`), and walks back to the trailhead (`Beat 5`).

## 4. System Sheet
- **Cutout Slab & Frozen Lake**: `11.2m × 0.85m × 11.2m` brown-earth foundation (`#5a3d2b`) with moss trim (`#4c6b3c`), sculpted snow banks (`#f4f7fb`), translucent blue-ice sheet (`#a9cbe0`), and a dark water fishing hole (`r = 1.05m`) ringed by slush blocks.
- **Flexing Cedar Fishing Rod + Line + Bobber**: 4-segment articulated rod parented to Finn's right wrist (`wristR`), dynamic catenary line to the red-and-white bobber, and concentric ice-hole ripple rings (`water.js`).
- **Leaping Silver-Teal Trout + Droplet Splash (`splash.js`)**: Multi-part articulated fish (body, dorsal fin,pectoral fins, wagging tail) that arcs out of the hole on a ballistic curve during `t = [8.0, 12.5]` while 18 water droplets and 3 expanding foam rings burst across the ice.
- **Red Thermos Steam & Swaying Snow Pines**: Rising voxel steam puffs from the thermos at `(2.05, 0.02, -0.85)` and wind-swaying tiered spruce cones + bare birch branches.

## 5. Beat Sheet (20.0s Seamless Loop)
- **Beat 1 (`0.0s – 4.5s`) — Cast & Settle**: Finn flicks his wrist to cast the red-white bobber into the center of the dark ice hole; a soft landing ring expands while Maya walks along the snowy ridge.
- **Beat 2 (`4.5s – 8.0s`) — The Bite**: The bobber twitches twice and plunges under the dark water; concentric ripple rings accelerate, Finn leans forward gripping the rod with both hands, and Maya stops and points.
- **Beat 3 (`8.0s – 13.0s`) — Breach & Splash**: Finn hauls back (`torso.x = -0.32`), the rod bends into a tight arc, and a silver-teal trout launches in a spinning parabolic arc above the ice hole amidst an 18-droplet water splash (`splash.js`) while Maya throws both arms up.
- **Beat 4 (`13.0s – 16.8s`) — Bucket Landing & High-Five**: The trout lands cleanly into the oak catch bucket (`(0.25, 0.02, -1.85)`) with a secondary lid bounce; Finn and Maya wave toward each other across the ice.
- **Beat 5 (`16.8s – 20.0s`) — Warm Thermos & Loop Seam**: Finn reaches for the steaming red thermos, takes a celebratory sip, and resets his rod posture as Maya returns to her starting snow-bank mark at `20.0s = 0.0s`.

