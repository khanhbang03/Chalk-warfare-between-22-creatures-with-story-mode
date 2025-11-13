# Chalk-warfare-between-22-creatures-with-story-mode
<img width="2377" height="1347" alt="Screenshot 2025-11-13 100240" src="https://github.com/user-attachments/assets/deeda86e-466a-46ef-bb82-29408279758f" />

🎬 Chalk Warfare — 22 Creatures: Story Mode (Cinematic Sequence)
Premise
![f45819d8813048d128cdce03972533a2](https://github.com/user-attachments/assets/0f925c68-124d-462d-8004-98d578d1c12e)
A ruined amphitheater of chalk (an old stadium) becomes the arena. 22 unique creatures — some humanoid, some fantastical — clash in a fast, cinematic free-for-all. The story mode is divided into four acts. Each act has triggers that automatically fire specific creature abilities, camera moves, and audio cues.

🐾 The 22 Creatures (short roster & abilities)

Each entry: Name — Role — Signature ability (1-line)

Ashen Drake — Sky striker — Molten Chalk Dive — flaming dive that leaves a burning chalk pool.

Frost Wisp — Ambusher — Glacial Veil — temporary area invisibility + slow.

Echohound — Scout — Sonic Chalk Bark — reveals hidden foes and knocks back.

Gale Harrier — Skirmisher — Chalk Gust — pushes enemies and clears particles.

Thorn Golem — Bulwark — Spine Wall — spawns a temporary chalk barricade.

Mirror Naiad — Illusionist — Duplicating Ripple — creates 3 short-lived clones.

Torchcap — Demolisher — Spore Burst — area bombardment of sticky chalk spores.

Sable Ranger — Sniper — Arc Line — long precision shot that pierces two targets.

Ivory Monk — Support — Healing Chalk Salve — heals nearby allies (or self).

Iron Finch — Tactician — Rail Trace — predictive rail shot with short cooldown.

Marrow Shade — Assassin — Silent Shard — instant-kill attempt on low-HP target (fails half the time).

Bloom Warden — Controller — Rootbind Chalk — slows and roots targets.

Cinder Chef — Wildcard — Flambé Grenade — explosive scatter projectiles that set terrain on chalk-fire.

Voyant Owl — Oracle — Foresee — marks upcoming targets for 6s on HUD.

Grotto Crab — Tank — Shellshock — spawns temporary reflective shell.

Vapor Sprite — Trickster — Mistwalk — teleport dash plus short confusion debuff.

Rune Stag — Leader — Call of Lines — increases attack speed of nearby allies for 8s.

Quartz Ant — Swarm — Fracture Swarm — spawns many micro-projectiles in cone.

Tempest Siren — Crowd-control — Chord of Chalk — global stagger wave (long cooldown).

Obsidian Pup — Speedster — Slide Strike — dash through enemies, leaving slipstream.

Lumen Priest — Finalist — Blinding Gospel — global flash that briefly disables active abilities.

Night Loom — Finale creature — Nether Trace — a singular cinematic “re-write” ability that momentarily alters battle gravity (used in climax).

(Each ability can be mapped to your simulator as an event that sets flags, spawns projectiles, modifies hit chances, or alters drawing/post-processing effects.)

⚖️ Suggested Stats (for quick simulator mapping)

Use simple integers to keep simulation light:

HP: most = 1 (one-hit) — heavies (Thorn Golem, Grotto Crab) = 3

Cooldown (s): quick abilities 6–12, big ultimates 20–40

Example mapping (you can import the JSON below to set fields):

{"name":"Ashen Drake","team":null,"hp":2,"cd":18,"ability":"moltenDive"}

{
 "roster":[
  {"name":"Ashen Drake","hp":2,"cd":18,"ability":"moltenDive"},
  {"name":"Frost Wisp","hp":1,"cd":12,"ability":"glacialVeil"},
  {"name":"Echohound","hp":1,"cd":8,"ability":"sonicBark"},
  {"name":"Gale Harrier","hp":1,"cd":10,"ability":"chalkGust"},
  {"name":"Thorn Golem","hp":3,"cd":20,"ability":"spineWall"},
  {"name":"Mirror Naiad","hp":1,"cd":14,"ability":"duplicate"},
  {"name":"Torchcap","hp":1,"cd":11,"ability":"sporeBurst"},
  {"name":"Sable Ranger","hp":1,"cd":9,"ability":"arcLine"},
  {"name":"Ivory Monk","hp":1,"cd":15,"ability":"salve"},
  {"name":"Iron Finch","hp":1,"cd":10,"ability":"railTrace"},
  {"name":"Marrow Shade","hp":1,"cd":16,"ability":"silentShard"},
  {"name":"Bloom Warden","hp":2,"cd":12,"ability":"rootbind"},
  {"name":"Cinder Chef","hp":1,"cd":10,"ability":"flambe"},
  {"name":"Voyant Owl","hp":1,"cd":18,"ability":"foresee"},
  {"name":"Grotto Crab","hp":3,"cd":22,"ability":"shellshock"},
  {"name":"Vapor Sprite","hp":1,"cd":9,"ability":"mistwalk"},
  {"name":"Rune Stag","hp":2,"cd":20,"ability":"callOfLines"},
  {"name":"Quartz Ant","hp":1,"cd":7,"ability":"fractureSwarm"},
  {"name":"Tempest Siren","hp":2,"cd":30,"ability":"chordOfChalk"},
  {"name":"Obsidian Pup","hp":1,"cd":8,"ability":"slideStrike"},
  {"name":"Lumen Priest","hp":2,"cd":40,"ability":"blindingGospel"},
  {"name":"Night Loom","hp":4,"cd":60,"ability":"netherTrace"}
 ]
}

(You can treat this as a free-for-all — team field null — or split into factions if you prefer.)

🎭 Story Mode — Act Structure & Timeline

Use this timeline to auto-trigger events. I give wall-clock seconds from the start; when you integrate into code, use these times (or scene indices if you prefer Next/Auto).

Act I — “The Awakening” (0:00 — 0:24)

0:00 — Camera Intro: slow crane-shot across frozen chalk seats to the arena center. Soft ambient choir. On-screen title fades.

0:04 — Narration: “When chalk remembers, beasts return…” (display subtitle for 4s).

0:06 — Spawn cues: All 22 creatures fade into existence (small puff particles).

0:10 — Minor skirmishes: Echohound, Sable Ranger, Vapor Sprite perform scouting moves (spawn small detection pings and reveal 2 hidden creatures).

0:18 — Shot: Mirror Naiad drops 3 clones (duplicates appear near water shadows). Play twinkling sound.

Act II — “The Rising Tumult” (0:24 — 1:10)

0:24 — Ashen Drake flies above; Molten Chalk Dive triggers at 0:28 — spawns 3 lava pools (area damage over 4s). Camera cliff cut to close-up. Play low boom.

0:32 — Bloom Warden roots several units crossing lava; root VFX (green chalk vines).

0:38 — Vapor Sprite Mistwalks behind Thorn Golem and places a Spine Wall sabotage — Thorn Golem spawns barrier but it’s corrupted (shorter lifespan).

0:45 — Tempest Siren charges chord (long-cue) — visual hum across arena (warning pulse).

0:52 — Sable Ranger Arc Line pierces three targets in line (visual tracer). If any are low-HP, Marrow Shade capitalizes and uses Silent Shard (attempt).

1:00 — Narration/Title Card: “Phase II — The Ground is Seasoned”

Act III — “The Turning” (1:10 — 2:10)

1:10 — Voyant Owl uses Foresee — show HUD markers (outline enemies that will be hit next 6s).

1:16 — Cinder Chef launches Flambé Grenade barrage (projectiles) — causes multiple small fires — visually add bloom and rising heat distortion.

1:22 — Obsidian Pup Slide Strike across a line of targets, leaving slipstreams that increase move speed for 3s.

1:30 — Iron Finch Rail Trace fires predictive shot — it always hits unless Lumen Priest’s Blinding Gospel is active. (Camera slow-mo on impact.)

1:40 — Lumen Priest prepares Blinding Gospel — create HUD countdown (3…2…1) — triggers at 1:44: disable active abilities for 4s; screen flash (white vignette). Great cinematic slow-mo of dust.

1:50 — Night Loom flickers; small gravity distortions (minor object drift) — tease final move.

Act IV — “The Finale” (2:10 — 3:00)

2:10 — Nether Build-up: Night Loom charges Nether Trace (long charge; show radial ring on arena; sound deep chime). Camera pulls back to wide shot.

2:25 — All surviving creatures converge on the Night Loom zone — simultaneous micro-skirmish montage (fast cuts).

2:40 — Night Loom unleashes Nether Trace: briefly inverts arena gravity for 2.5s and applies a “rewrite” filter where all remaining HP values are re-evaluated with a final damage pulse (cinematic — bright chalk sigil rises). Use a dramatic musical sting and deep rumble.

2:46 — Aftermath slow-mo: survivors tumble, glow, then dissolve into chalk silhouettes. Camera slowly zooms into one surviving creature (if any) or the empty chalk sigil.

2:55 — Narration: “Taste remembered, lines redrawn.” Fade to title card and credits roll.
