# Cinematic Visual Generation

A Codex skill for turning story beats, scenes, portraits, and products into cinematic image-generation prompts with intentional camera language—without relying on glossy, generic “AI film still” styling.

It is particularly useful for storyboards, micro-films, key art exploration, and grounded visual narratives.

## What it does

- Turns a narrative beat into a camera-aware generation prompt.
- Chooses framing, practical lighting, palette, texture, and exclusions that support the scene.
- Maintains character, wardrobe, prop, location, time, and palette continuity across a sequence.
- Provides a grounded independent-film baseline for naturalistic results: available light, lived-in locations, contained performance, normal skin texture, and imperfect framing.
- Provides focused recipes for quiet drama, night exteriors, action, landscapes, and product images.

## Install

Copy the skill folder into your Codex skills directory:

```powershell
Copy-Item -Recurse .\cinematic-visual-generation "$HOME\.codex\skills\cinematic-visual-generation"
```

Restart or refresh Codex so it discovers the new skill.

## Use

Invoke it explicitly:

```text
Use $cinematic-visual-generation to create a 6-shot micro-film storyboard about a night-shift worker returning a lost key.
```

Or make a natural-language request such as:

```text
Generate a grounded, quiet cinematic frame of someone waiting for the last bus in rain.
```

For each frame, provide a subject, action, setting, and feeling when you have them. The skill fills in ordinary production details and uses image generation for final visuals.

## Grounded independent-film mode

Use this mode when a result feels over-styled or “too AI.” It favors:

- Eye-level 35–50 mm framing with partial occlusion or a slightly awkward crop.
- Available light from a window, streetlamp, fluorescent tube, or carriage.
- Muted, realistic color; normal skin and fabric texture; believable exposure.
- Small actions rather than posed emotion.

Example:

```text
Use $cinematic-visual-generation. A woman waits alone at a worn suburban station in light rain. Keep it observational and low-saturation: available fluorescent light, an off-centre 40 mm frame, chipped paint, wet tiles, unretouched skin, no glamour or poster composition.
```

## Project layout

```text
cinematic-visual-generation/
├── SKILL.md                    # Trigger description and core workflow
├── agents/openai.yaml           # Codex UI metadata
└── references/shot-recipes.md   # Reusable visual and correction recipes
```

## Scope and limitations

This skill shapes prompts and visual decisions. Image-generation models can still vary in identity consistency, prop details, and legible text; iterate by correcting the largest mismatch rather than adding stacks of adjectives. Do not request imitation of a living artist’s recognizable style.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Please keep `SKILL.md` concise and move detailed, reusable recipes into `references/`.

## License

Released under the [MIT License](LICENSE).
