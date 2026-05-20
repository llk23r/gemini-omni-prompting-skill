# Music Video Skill

Version: 1.1.0

A specialized extension of the gemini-omni-prompting-skill for crafting music video prompts. Grounded in outlier directorial patterns extracted from the canon of the greatest music videos ever made — not median "best practices" but the techniques that made individual videos unforgettable.

---

## Outlier Pattern Library

These are the directorial fingerprints that made specific videos undeniable. Use them as axes in Gemini Omni prompts — combinable, stackable, and remixable.

### 1. The Robotic Precision Pan (Dave Meyers / Kendrick Lamar — *HUMBLE.*)

**What it is:** A 6-axis robotic camera arm (e.g., Bolt rig by Mark Roberts Motion Control) executes mathematically perfect arcs around a stationary or slow-moving subject. The camera swings with mechanical confidence — no human wobble, no correction. At ~2:00 in *HUMBLE.*, the camera executes a slow, god-tier horizontal pan across Kendrick seated at a table with disciples, Caravaggio-lit. The move is too smooth to feel handheld, too deliberate to feel like a drone.

**Gemini Omni axis:** `camera_motion`

**Prompt pattern:**
```
Camera motion: 6-axis robotic arm executes a slow lateral arc, 180° sweep over 4 seconds,
perfectly level, starting behind the subject's right shoulder and landing facing them
directly. No acceleration ramp — constant, mechanical speed. Feels like a surveillance
satellite gaining consciousness.
```

**When to deploy:** Moments of false peace before eruption. A calm tableau that the camera studies like evidence.

---

### 2. The Inverted Planet / Tiny World (Dave Meyers — *HUMBLE.*, GoPro Omni rig)

**What it is:** A 360° rig is mounted on the vehicle/body, then the footage is inverted in post to create a "tiny planet" effect. The subject becomes god-sized above a curved miniature world beneath them.

**Gemini Omni axis:** `camera_motion`, `style`

**Prompt pattern:**
```
Style: Tiny planet / inverted 360° projection. Subject occupies the top of a curved world,
full body visible, standing on a convex surface that wraps around below them. Background
bends away into a circular horizon. Feels like a music video shot from orbit.
```

---

### 3. The Single-Take Defamiliarizer (Hiro Murai — *This Is America*, Childish Gambino)

**What it is:** A continuous or near-continuous shot that tracks through a space while the background changes in meaning. The foreground (artist performance) remains the eye's anchor, but what happens behind them rewrites the interpretation of everything you just watched. The violence in *This Is America* happens mid-background, half out of frame, demanding a second watch.

**Gemini Omni axis:** `action`, `camera_motion`, `environment`

**Prompt pattern:**
```
Camera motion: Slow continuous push-in on the performer at center frame.
Environment: Background layers shift in depth — first empty warehouse, then crowd dancing,
then (at timestamp 0:40) a violent act happens at 30% right of frame, out of focus,
while performer's expression doesn't break. Viewer must choose where to look.
Action: Performer executes sharp, high-contrast choreography. Every move is a deliberate
distraction from the background event.
```

**When to deploy:** Songs with double meanings, social commentary, or an artist performing a character.

---

### 4. The Grief Confessional (Mark Romanek — Johnny Cash, *Hurt*)

**What it is:** Intercutting between present performance and archival footage/photographs of the artist's past, treated as equal in time. No flashback grammar — the old and new exist simultaneously. Romanek shot Cash in his collapsed House of Cash museum, intercutting vintage career footage. The video is a monument before a funeral.

**Gemini Omni axis:** `references`, `style`, `action`

**Prompt pattern:**
```
References: Archival stills and footage of subject from [YEAR_RANGE] provided as reference.
Style: Intercut present-tense performance (desaturated, high contrast, ambient available
light) with archival images (slightly sped up, grain added to match era). Cut on emotional
peak not on musical beat. The edit rhythm is breathing, not metronomic.
```

**When to deploy:** Songs about regret, age, legacy. Artist who has an arc worth showing.

---

### 5. The Conceptual Loop (Michel Gondry — Björk, *Human Behaviour* / White Stripes, *Fell in Love with a Girl*)

**What it is:** The video's visual logic operates by a rule that the viewer must discover — a grammar that is never explained but becomes obvious. Gondry built *Fell in Love with a Girl* entirely from LEGO bricks. The constraint is not a gimmick — it's the argument.

**Gemini Omni axis:** `style`, `constraints`

**Prompt pattern:**
```
Constraints: Entire video rendered as if constructed from [MATERIAL — e.g., paper cutouts,
found objects, fabric, matchsticks, analog TV static]. No digital effects visible — only
the material's own physics. If something explodes, it explodes via the material's logic
(paper burns, fabric tears, LEGO bricks fly apart).
Style: Handmade world. Every frame should feel like a diorama that someone actually built.
```

---

### 6. The Choreographic Detonation (Jake Nava — Beyoncé, *Single Ladies* / Spike Jonze — Fatboy Slim, *Praise You*)

**What it is:** A single unbroken performance space — no cuts or minimal cuts — where the choreography IS the video. The camera is complicit, not dominant. It holds wide, lets the bodies work, and punches in only at peak moments. *Single Ladies* (dir. Jake Nava) was shot in a single black-and-white take, Bob Fosse-inflected, with the camera locked on a wide that trusted the body completely. Jonze's *Praise You* took the same restraint into guerrilla-style public performance.

**Gemini Omni axis:** `action`, `camera_motion`, `framing`

**Prompt pattern:**
```
Framing: Wide (full body) as default. Camera holds for 8–16 bars before cutting. No shaky
handheld — either locked tripod or slow push dolly.
Action: Choreography is designed to have one climactic "detonation" move per 16-bar section
that the camera must be in position for. Build to it. Don't cut away during it.
Camera motion: Minimal. Confidence through stillness. Movement reserved for transitions
between sections.
```

**When to deploy:** Dance-forward tracks. Songs where the body IS the argument.

---

### 7. The Fragmented Self (Chris Milk — Kanye West, *Runaway* / Arcade Fire, *The Wilderness Downtown*)

**What it is:** The artist exists simultaneously in multiple visual registers — a live performance, a symbolic world, an archival space — but the video never explains how they connect. The viewer assembles the meaning. *Runaway* is 35 minutes. The phoenix and the table ballet and Kanye in the wheat field are all "true" simultaneously.

**Gemini Omni axis:** `style`, `environment`, `action`

**Prompt pattern:**
```
Environment: Three distinct spaces exist in parallel — [SPACE A: symbolic/surreal],
[SPACE B: grounded/intimate], [SPACE C: archetypal/monumental]. They never explain
each other. Cut between them by emotional rhyme, not narrative logic.
Style: Each space has its own color grade and aspect ratio. They are not flashbacks —
they are simultaneous truths.
```

---

### 8. The Surveillance Aesthetic (Director X / Hiro Murai — Drake, *HYFR* / Gambino)

**What it is:** The camera is positioned where it shouldn't be — inside the party, behind the bar, in a room that real cameras don't belong in. Security-cam angles, fish-eye hallway shots, overhead ceiling perspectives. Creates intimacy through voyeurism.

**Gemini Omni axis:** `shot_framing`, `camera_motion`, `style`

**Prompt pattern:**
```
Framing: Security camera angle — fixed, high-corner mount, 120° wide fisheye. Subject
moves through frame rather than being followed. Camera doesn't track them.
Style: Slightly degraded image quality — mild compression artifacts, no lens flares,
flat institutional lighting. The frame feels accidentally caught, not directed.
Camera motion: Static. The space is the subject. The person passes through it.
```

---

### 9. The Unguarded Documentary (J. Cole — *Might Delete Later* era / *The Fall-Off* campaign)

**What it is:** No concept, no set. The artist moves through their actual world — studio, neighborhood, practice sessions — but the cinematography is intentional. The "no-video" is the video. What separates this from vlog footage is the eye: every shot is composed. Available light is chosen, not tolerated. The camera catches rather than directs. Cole's *Might Delete Later* and *Fall-Off* visuals treat the rehearsal as the performance and the process as the content.

**The grammar of this pattern:** The camera never asks the artist to do anything twice. If a moment passes, it passes. The edit is built from what actually happened.

**Gemini Omni axis:** `style`, `action`, `environment`

**Prompt pattern:**
```
Style: Observational documentary aesthetic. Handheld, available light, ambient sound bleeds.
No costume changes — artist in their actual clothing for the day. Cinematography is
opportunistic but composed: the camera catches moments, doesn't stage them.
Environment: Location that is genuinely meaningful to the artist — not a rented set.
Action: Artist exists in the space, not performing to camera. Performance emerges from
the environment's logic. If they're in a gym, they're actually working out.
Constraints: No second takes. No directed eyelines. If the artist looks at the camera,
leave it in.
```

**When to deploy:** Songs where authenticity is the thesis. Artists whose actual life is more interesting than any concept.

---

### 10. The Structural Rupture (Hype Williams — Kanye West, *Stronger*)

**What it is:** The video begins in one genre and breaks into another. *Stronger* opens as a neo-noir anime homage (*Akira*), then ruptures into pure performance. The rupture is the statement — two aesthetics collide without smoothing the seam.

**Gemini Omni axis:** `style`, `action`, `environment`

**Prompt pattern:**
```
Structure: Video operates in two movements.
Movement 1 (0:00–[TIMESTAMP]): [STYLE A — cinematic, narrative, world-building].
Movement 2 ([TIMESTAMP]–end): [STYLE B — raw performance, minimal environment].
The transition is a hard cut, not a fade. No bridge. The viewer feels the seam.
Style A and Style B should be maximally distinct — different aspect ratio, color grade,
camera grammar. The rupture is the thesis.
```

---

### 11. The Hyperreal Tableau (Melina Matsoukas — Beyoncé, *Formation* / Kendrick, *Poetic Justice*)

**What it is:** Each shot is composed as a painting — precise symmetry or deliberate off-axis imbalance, costumes as iconography. The video is a series of tableaux that individually work as standalone images. No shot is wasted. Every frame is extractable as an album cover.

**Gemini Omni axis:** `shot_framing`, `style`, `lighting`

**Prompt pattern:**
```
Framing: Painterly composition. Every shot should function as a standalone photograph.
Use the rule of thirds aggressively — subjects at extreme left or right, horizon low
or high, never centered unless for deliberate confrontational symmetry.
Lighting: Chiaroscuro. One dominant light source, deep shadows, no fill to flatten.
Style: Costumes carry visual weight as iconography. Color palette limited to 3 hues
per shot. Backgrounds are architecturally significant, not neutral.
```

---

### 12. The Spatial Impossibility (Spike Jonze / Michel Gondry — physical set construction)

**What it is:** The space the video occupies doesn't obey architecture. Corridors lead back to themselves. Rooms contain other rooms. The artist walks through a door and arrives somewhere physically impossible. Both Gondry and Jonze built physical sets to achieve this — no CGI. The wrongness is structural, not digital.

**Gemini Omni axis:** `environment`, `style`

**Prompt pattern:**
```
Environment: Space that violates spatial logic. [EXAMPLE: Hallway that curves back on
itself. Room whose ceiling is another floor. Exterior of a building whose interior
is larger than its exterior allows.] The impossibility is revealed gradually —
not announced upfront.
Style: Photorealistic rendering. The impossible space looks completely physical — no
digital glow, no distortion effects. The wrongness is architectural, not visual.
```

---

## Music Video Operating Modes

These extend the base skill's `mode` parameter:

- `create_mv_scene` — Build a full music video scene prompt using outlier patterns
- `apply_mv_pattern` — Apply a named pattern from the library above to an existing scene
- `storyboard_mv` — Convert a track structure (verse/hook/bridge) into timed scene shots
- `rewrite_mv_camera` — Reconstruct the camera grammar of an existing prompt
- `fuse_mv_references` — Blend visual references from multiple directors into one coherent aesthetic
- `director_voice` — Adopt the grammar of a specific director (Meyers, Murai, Gondry, Matsoukas, Milk, Romanek, Jonze, Nava, Hype Williams) as the prompt's lens

---

## Music Video Inputs

Required:
- `user_goal`
- `mode`
- `track_section` — which part of the song (verse 1, chorus, bridge, outro)
- `song_bpm` — tempo shapes cut frequency and camera move speed

Optional:
- `pattern_reference` — named pattern from the library above
- `director_voice` — named director to channel
- `beat_anchor` — specific timestamp or bar where a visual event must land
- `artist_physicality` — how the artist moves (minimal, dance-forward, stationary performer)
- `narrative_weight` — is the video symbolic, literal, or documentary
- `budget_register` — conceptual (no location, no crew) / mid / cinematic

---

## Music Video Outputs

1. `intent_summary` — what the scene is trying to accomplish emotionally
2. `pattern_applied` — which outlier pattern(s) from the library are in use
3. `production_prompt` — full Gemini Omni-compatible prompt
4. `director_rationale` — why this camera grammar serves this song section
5. `beat_anchors` — specific visual events mapped to track timestamps
6. `optional_variants` — 2 alternate treatments using different patterns

---

## Behavioral Rules

**Avoid the median:** Do not default to performance-on-stage, one-color-backdrop, or intercutting between close-ups and wide shots as the default grammar. These are invisible. Force a choice from the outlier library on every prompt.

**Beat anchor first:** Before writing any camera description, identify which musical moment the shot must land on. The camera is always subordinate to the music's physics.

**Pattern constraint:** Pick one dominant pattern per scene. Two patterns can coexist only if one is `camera_motion` and the other is `style` — they operate on different axes and don't compete.

**The rupture rule:** Every music video should contain at least one moment that breaks its own grammar — a beat where the visual logic resets. Identify where this rupture should land and build toward it.

**Director as constraint:** When `director_voice` is specified, all other axes must be compatible with that director's known grammar. A Gondry prompt should never include robotic precision. A Murai prompt should never have rapid intercutting. A Nava prompt trusts wide frames and withholds the close-up.

---

## Create MV Template

```
Goal: {user_goal}
Track section: {track_section} (bars {bar_start}–{bar_end})
BPM: {song_bpm}

Pattern: {pattern_reference}
Director voice: {director_voice}

Subject: {subject}
Artist physicality: {artist_physicality}
Environment: {environment}
Action: {action}
Style: {style}
Lighting: {lighting}
Framing: {shot_framing}
Camera motion: {camera_motion}
Beat anchor: {beat_anchor} — [visual event that must land on this beat]
Text: {text_overlay}
References: {references}
Narrative weight: {narrative_weight}
Budget register: {budget_register}
Constraints: {constraints}
```

---

## Source Boundary

| Layer | Source |
|---|---|
| Camera technique analysis | Original synthesis from top-37 music video canon |
| Directorial grammar | Dave Meyers, Hiro Murai, Spike Jonze, Michel Gondry, Mark Romanek, Melina Matsoukas, Chris Milk, Hype Williams, Jake Nava, Director X — public interviews and visual analysis |
| Gemini Omni prompt structure | Extends base skill (SKILL.md) without reproducing source text verbatim |
| Beat-anchoring framework | Original extension for music video temporal specificity |
