# Music Video Skill — Example Prompts

Full end-to-end examples showing the music video skill firing across different patterns, director voices, and track sections.

---

## Example 1 — Robotic Precision Pan / Dave Meyers voice

**Input:**
```
mode: create_mv_scene
user_goal: Verse 2 of a trap track about control. Artist seated at a long table, alone.
track_section: Verse 2 (bars 17–32)
song_bpm: 140
pattern_reference: Robotic Precision Pan
director_voice: Dave Meyers
budget_register: cinematic
```

**Output:**

`intent_summary:` The camera performs power for the artist. The verse is about dominion — the shot should feel like a deposition. Nobody else is present but the camera's arc implies there should be.

`pattern_applied:` Robotic Precision Pan

`director_rationale:` Meyers uses the Bolt rig to make stillness feel volatile. The mechanical arc transforms a seated figure into the fixed point of a rotating world. At 140 BPM with a trap hi-hat grid, the camera move runs deliberately against tempo — slow, sovereign, indifferent to the beat.

`beat_anchors:`
- Bar 17: Camera begins behind artist's right shoulder, slightly above eye level
- Bar 24 (drop / hook word): Camera is directly facing artist — full frontal, dead center
- Bar 32 (verse end): Camera has completed its arc and arrived at the left profile

`production_prompt:`
```
Goal: Verse 2 of a trap track about control. Artist seated at a long table, alone.
Track section: Verse 2 (bars 17–32)
BPM: 140

Pattern: Robotic Precision Pan
Director voice: Dave Meyers

Subject: Male artist, 20s, seated at the center of an 8-person dining table, dressed
in white. Posture is upright but relaxed. Hands resting on the table surface.
Environment: Baroque dining hall, European interior. Empty chairs at every seat.
Tapered candles lit along the full length of the table. Ceiling recedes into darkness.
Action: Artist does not move. Delivers bars with minimal facial expression — controlled,
not cold. Eyes tracking offscreen, not to camera.
Style: Caravaggio lighting. Single warm key source at camera-left, 45° above eye line.
Everything outside the key pool falls into near-total shadow. No fill. No ambient bleed.
Lighting: Practical candles plus one off-screen 2K tungsten as key. No LED softboxes.
Color temperature: 2700K throughout. No blue.
Framing: Medium wide. Full table length visible. Artist at geometric center of frame.
Camera motion: 6-axis robotic arm (Bolt rig or equivalent). 180° lateral arc over the
full 16 bars. Constant velocity — no ease-in, no ease-out. The move starts behind the
artist's right shoulder and concludes at the left profile. Camera height stays fixed at
slightly above eye level throughout the arc.
Beat anchor: Bar 24 (drop) — camera faces artist directly at this exact moment. The
frontal frame holds for 2 bars before continuing the arc.
Constraints: No cuts during the arc. Single continuous take for the full verse.
No camera shake. If the robotic arm introduces vibration, stabilize in post.
```

`optional_variants:`
1. **Surveillance Aesthetic variant** — replace the Bolt arc with 4 fixed security-cam angles mounted at ceiling corners of the room. Cut between them on every 4th bar. The artist never looks at any of the cameras.
2. **Hyperreal Tableau variant** — abandon the arc entirely. Lock the camera at the far end of the table, 35mm lens, and hold the single frame for all 16 bars. The artist and the empty chairs become a painting. Cut only at the verse end.

---

## Example 2 — Fragmented Self / Hiro Murai voice

**Input:**
```
mode: create_mv_scene
user_goal: Chorus of a soul track about living two lives. Artist appears as two versions of herself that exist in different spaces.
track_section: Chorus (bars 33–48)
song_bpm: 92
pattern_reference: Fragmented Self
director_voice: Hiro Murai
artist_physicality: minimal
narrative_weight: symbolic
budget_register: mid
```

**Output:**

`intent_summary:` The chorus argues that both versions of this person are real and neither is the performance. The video can't resolve which space is "true" because the point is that both are.

`pattern_applied:` Fragmented Self

`director_rationale:` Murai's signature is emotional precision through formal stillness. He withholds close-ups until they cost something. The locked camera in both spaces makes the cuts feel structural, not editorial — you're not being taken somewhere, you're being shown that two places exist simultaneously.

`beat_anchors:`
- Chorus downbeat (bar 33): First cut to Space A
- Every recurrence of hook word: Cut between spaces on the syllable
- Final bar (bar 48): Hold on Space B. Artist's eyeline drifts toward camera for the first time. Cut to black on the last note.

`production_prompt:`
```
Goal: Chorus of a soul track about duality. Two simultaneous versions of the artist.
Track section: Chorus (bars 33–48)
BPM: 92

Pattern: Fragmented Self
Director voice: Hiro Murai

Subject: Female artist, 30s. Two versions — same costume, same hair, no distinction
between them except their environment and behavior.
Environment A (Space A): Empty swimming pool, mid-afternoon, Los Angeles. Concrete walls.
Blue residue staining at the waterline. Flat overcast sky above.
Environment B (Space B): Dense second-growth forest, Pacific Northwest. Overcast.
Moss on every surface. No clearings visible.
Action: Space A — artist moves slowly, tracing the pool wall with one hand. Not dancing.
Space B — artist stands completely still, looking at something just out of frame.
They never acknowledge each other or the camera — until the final bar.
Style:
  Space A: Color grade — bleached cyan and white, slightly overexposed. Skin tones warm.
  Space B: Color grade — desaturated green-brown, crushed blacks, cool shadows.
Lighting:
  Space A: Available overcast daylight. No additions.
  Space B: Available overcast daylight through canopy. No additions.
Framing: Both spaces use identically composed medium shots. Same focal length (50mm).
Same distance from subject. The formal symmetry makes the visual difference feel violent.
Camera motion: Locked in both spaces. No movement whatsoever.
Beat anchor: Hook word — hard cut between spaces on every syllable occurrence.
Final bar: Hold Space B. Artist's eyes move to lens. Hold 2 seconds after the last note.
Constraints: The two versions are never in the same frame. No CGI split-screen.
No dissolves between spaces — only hard cuts.
```

`optional_variants:`
1. **Unguarded Documentary variant** — shoot both spaces handheld, available light, without the artist knowing the exact shot. Let the environment determine where the camera goes. The "two lives" idea survives; the formal symmetry dissolves into something rawer.
2. **Structural Rupture variant** — run the chorus in Space A only, then on the final chorus rupture into Space B with a different aspect ratio (1.33:1 → 2.39:1). The spaces stop alternating and one wins.

---

## Example 3 — Unguarded Documentary / Cole aesthetic

**Input:**
```
mode: create_mv_scene
user_goal: Full song visual. Artist in their home city. No concept — the place and the person are the concept.
track_section: Full song
song_bpm: 88
pattern_reference: Unguarded Documentary
artist_physicality: minimal
narrative_weight: documentary
budget_register: conceptual
```

**Output:**

`intent_summary:` Authenticity as argument. The video earns its lack of concept by making the observation precise. Every shot has to be good enough to justify the absence of a set.

`pattern_applied:` Unguarded Documentary

`director_rationale:` This pattern lives or dies on the quality of the eye. Without a concept to lean on, the cinematographer must find geometry in real spaces — a stairwell becomes a frame, a chain-link fence becomes a lighting rig. The constraint (no staging, no second takes) is what makes it work. The moment you ask the artist to do something again, you've lost.

`beat_anchors:`
- Verse 1: Artist in motion — walking, driving, entering a space
- Hook: Cut to still — artist seated or stationary. The energy contracts.
- Verse 2: Interior space. Tighter, more personal.
- Bridge: Something unexpected. The one moment in the shoot where the environment delivered something unplanned. Keep it regardless of whether it "fits."
- Outro: Pull back. The person is small in the space. Hold.

`production_prompt:`
```
Goal: Full song visual. Artist in their actual city. No constructed concept.
Track section: Full song
BPM: 88

Pattern: Unguarded Documentary

Subject: Artist in their actual clothing for the shoot day. No wardrobe.
Environment: Artist's real neighborhood, real frequented spaces — not chosen for aesthetics.
If they grew up there, the camera finds out what that looks like architecturally.
Action: Artist moves through spaces as they actually would. The camera follows without
directing. Conversation is allowed. Silence is allowed. Boredom is allowed.
Style: Handheld. Available light exclusively. Grain is acceptable — do not correct it.
No color grade that removes the location's actual color palette.
Lighting: Whatever is there. If it's harsh noon sun, work with the shadows it makes.
If it's a fluorescent-lit bodega, shoot in it.
Framing: Opportunistic but composed. The operator looks for geometry in the real space —
architectural frames within the frame, natural leading lines, accidental symmetry.
Camera motion: Handheld. No gimbal — some instability is honest.
Constraints: No second takes requested from the artist. One camera. No art direction
of the environment. If a stranger walks through the frame, leave it in.
```

`optional_variants:`
1. **Grief Confessional variant** — intercut the present-day location footage with archival photographs or home video from the same neighborhood. No explanation of the relationship between them.
2. **Surveillance Aesthetic variant** — supplement the handheld footage with actual security camera angles sourced from the location (with permission). The mix of camera qualities becomes the texture of the video.
