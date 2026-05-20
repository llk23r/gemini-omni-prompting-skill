# gemini-omni-prompting-skill

A portable, model-agnostic skill for structured multimodal video prompting and iterative scene editing.

Grounded in the [Gemini Omni prompt guide](https://deepmind.google/models/gemini-omni/prompt-guide/).

## What it does

- Turns a rough scene idea into a structured prompt
- Edits a scene without rewriting the whole thing
- Controls framing, camera, action, style, and text as separate axes
- Fuses image, video, audio, and storyboard references
- Preserves continuity across iterative edits

## Structure

```
gemini-omni-prompting-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── examples/
│   ├── create-scene.md
│   ├── iterative-edit.md
│   ├── camera-rewrite.md
│   ├── action-rewrite.md
│   ├── text-rendering.md
│   ├── reference-fusion.md
│   ├── style-transfer.md
│   └── storyboard-to-video.md
├── docs/
│   └── source-boundary.md
└── tests/
    └── behavioral-cases.md
```

## Usage

1. Pick a mode: `create_scene`, `edit_scene`, `rewrite_camera`, etc.
2. Provide a goal and any references.
3. Mark what must stay fixed.
4. Generate the prompt or edit delta.
5. Iterate conversationally.

## Sources

- Core behavior: [Gemini Omni prompt guide](https://deepmind.google/models/gemini-omni/prompt-guide/)
- General prompt structure: [Google Cloud prompt engineering guide](https://cloud.google.com/discover/what-is-prompt-engineering)
- Optional image extensions: [Gemini Image prompt guide](https://deepmind.google/models/gemini-image/prompt-guide/)

## License

Apache 2.0
