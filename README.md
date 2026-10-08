# NEON STUFFER

A synthwave, top-down 3D physics game about **putting stuff inside of stuff**, at night, in a neon city full of traffic, with a soundtrack that is **generated live** in your browser.

**Play:** https://pascalnet.github.io/neon-stuffer/

## How to play
- Fly the tractor-beam drone, grab things (crates, balls, cones, barrels, toy cars, even boxes) and throw them into containers: dumpsters, open boxes, THE VAULT (open-roof tower, x1.5), and **moving pickup trucks** (x2).
- Stuff things into a box, then stuff that box into something else for nesting bonuses. Score again within 5 s to build combos.
- 6 levels: Warm Up, Box in a Box, Drive-Thru, The Vault, Combo King, then an endless 120 s Neon Frenzy score attack (best score saved).

**Desktop:** WASD/arrows to fly · Space/E or click to grab/drop · click to throw at the cursor (snaps to nearby containers) · Q auto-aim throw · M mute · R respawn objects.
**Phone/tablet:** left-thumb virtual joystick · GRAB / THROW buttons (throw auto-aims ahead) · or tap the city to throw at that spot. Portrait and landscape both work.

## Procedural synthwave music
No audio files. Everything is synthesized with the Web Audio API on a lookahead scheduler (100-110 BPM, seeded RNG): driving octave sawtooth bass with filter envelopes, kick with sidechain pumping, gated-reverb snare, hats, lush detuned pad chords (minor progressions such as i-VI-III-VII), arpeggiated lead, a melodic lead, a generated convolver reverb and a dotted-eighth delay. Sections (intro / build / drop / breakdown), progressions, arp patterns and melodies are varied procedurally. The music reacts to play: scoring fires beat-quantized stingers, combos open the filters and push the intensity, and clearing a level forces a drop. Add `?seed=1234` to the URL to replay a specific song and city.

## Tech
Single `index.html`: three.js 0.160 (with UnrealBloom postprocessing) and cannon-es 0.20 loaded from the jsDelivr CDN through an import map. No build step.
