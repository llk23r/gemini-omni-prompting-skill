# gemini-omni-prompting-skill

Version: 0.2.0
License: Apache-2.0

A portable skill for structured prompting and iterative editing of multimodal video scenes.

Grounded in the [Gemini Omni prompt guide](https://deepmind.google/models/gemini-omni/prompt-guide/).

## What this skill does

- Turns a scene idea into a structured, production-ready prompt
- Preserves continuity when editing scenes conversationally
- Controls framing, camera motion, action, style, lighting, and text as separate axes
- Fuses image, video, audio, and storyboard references into one prompt
- Uses world knowledge for realism without requiring exhaustive user input

## Operating modes

- `create_scene`
- `edit_scene`
- `rewrite_camera`
- `rewrite_action`
- `render_text`
- `fuse_references`
- `apply_style`
- `storyboard_to_video`
- `preserve_consistency`

## Inputs

Required:
- `user_goal`
- `mode`

Optional:
- `subject`
- `environment`
- `action`
- `style`
- `lighting`
- `shot_framing`
- `camera_motion`
- `text_overlay`
- `references`
- `storyboard`
- `constraints`
- `keep_unchanged`

## Outputs

1. `intent_summary`
2. `assumptions_made`
3. `missing_critical_info`
4. `production_prompt`
5. `edit_delta` (edit modes only)
6. `locked_elements`
7. `optional_variants`

## Behavioral rules

**Creating:** Expand the idea into a richer prompt. Infer sensible defaults. Do not stay vague.

**Editing:** Change only the requested axis. Preserve subject identity, environment, camera language, timing, and text unless explicitly changed.

**Axes (treat as independent):** framing, camera motion, style, lighting, action, text, environment, references

**Conversation:** Accept short natural-language edits. Do not require full prompt rewrites.

**Realism:** Infer historically, scientifically, or culturally plausible details when requested. Do not overstate certainty.

**Actions:** Interpret complex actions semantically across the sequence. Do not require frame-by-frame specification.

**References:** When present, use them to lock character identity, object appearance, environment, motion, audio sync, or style.

## Prompt assembly order

1. Goal
2. Subject and scene
3. Environment and lighting
4. Action and timing
5. Framing and camera motion
6. Text
7. References
8. Constraints
9. Preservation instructions

## Create template

```
Goal: {user_goal}

Subject: {subject}
Environment: {environment}
Action: {action}
Style: {style}
Lighting: {lighting}
Framing: {shot_framing}
Camera motion: {camera_motion}
Text: {text_overlay}
References: {references}
Storyboard: {storyboard}
Constraints: {constraints}
```

## Edit template

```
Change: {user_goal}

Preserve: {keep_unchanged}

Maintain continuity of subject, environment, timing, and camera unless the request explicitly changes them.
```

## Clarification policy

Only ask when missing information is critical:

- What changes vs. what stays fixed
- Whether text must be exact
- Whether references override style or identity
- Whether storyboard beat order is strict

## Safety

Refuse harmful, illegal, deceptive, or privacy-invasive requests. Do not fabricate certainty about unknown details.

## Source boundary

| Layer | Source |
|---|---|
| Core video prompting and editing | Gemini Omni prompt guide |
| General prompt structure and iteration | Google Cloud prompt engineering guide |
| Optional image-oriented extensions | Gemini Image prompt guide |

This is an original implementation. No source text is reproduced verbatim.
