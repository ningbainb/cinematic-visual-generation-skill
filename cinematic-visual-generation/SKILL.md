---
name: cinematic-visual-generation
description: Turn concepts, scenes, products, portraits, story beats, micro-film storyboards, and shot lists into cinematic image-generation prompts with intentional composition, lighting, camera language, color grading, atmosphere, and visual continuity. Use when a user asks for movie-like, filmic, cinematic, director-style, dramatic, story-driven, cinematic storyboard, 分镜, 故事板, 微电影, 电影感, 真实感, or 去 AI 味 visual generation or image edits.
---

# Cinematic Visual Generation

Create images that feel like a deliberate film frame, not a list of attractive effects. Use the available image-generation tool for generation and editing.

## Workflow

1. Identify the requested deliverable: one frame, a prompt only, or a multi-shot storyboard. For a multi-shot request, treat each shot as a separate image by default; never substitute a contact sheet, collage, or post-hoc crop unless explicitly requested.
2. Identify the frame's subject, action, emotional beat, setting, and intended viewer feeling. Infer ordinary missing details; ask only if an unresolved choice would change the result materially.
3. Choose one visual grammar that supports the beat: shot size, camera angle, lens character, depth of field, lighting motivation, palette, atmosphere, and composition.
4. Build one coherent prompt in this order: subject and action; environment; framing and camera; lighting; palette and texture; mood; exclusions. Prefer concrete visual evidence over adjectives.
5. For a series, write a **Continuity Lock** once and repeat it verbatim in every shot prompt. Lock identity, hair, wardrobe, key prop, location, time/weather, and base palette; vary only the shot-specific action, framing, and available light.
6. Generate each requested image independently. If an image reference is available, use it for continuity, not as permission to merge frames or copy a contact sheet layout.
7. If iterating, diagnose the single biggest mismatch (story clarity, framing, light, identity, or realism) and make a targeted change rather than stacking more modifiers.

### Style priority

Resolve conflicts in this order: **explicit user request > story/emotional beat > selected recipe > default cinematic language**. Select one primary recipe per frame. Do not combine grounded documentary constraints with neon noir or epic rim-light conventions unless the user explicitly asks for that hybrid.

## Prompt Standard

Write the final generation prompt in English unless the user requests another language. Keep it as natural visual direction, usually 80–180 words. Include only details that improve the frame.

Use this compact pattern:

```text
[Shot and subject]: [person/object] [doing what], [specific setting and story clue].
[Camera]: [shot size], [angle], [lens or depth behavior], [composition].
[Light]: [motivated source], [contrast and shadow behavior].
[Look]: [palette], [texture/medium], [atmosphere], [emotional tone].
Avoid: [only likely failure modes].
```

For sequences, prepend this block to every prompt:

```text
Continuity Lock: [identity and age], [hair and wardrobe], [key prop], [location], [time/weather], [base palette]. Keep these unchanged across all shots.
Shot Delta: [only this shot's action, framing, camera position, and motivated light change].
```

### Grounded realism guardrails

For naturalistic drama, state **what the camera happens to catch**, not what an idealized poster should look like. Ground each frame in one ordinary, imperfect detail: rain stuck in hair, a creased sleeve, uneven fluorescent spill, dirty platform tiles, a slightly missed focus pull, or a partially obscured face.

- Use one lighting source and a restrained palette. Avoid piling up `cinematic`, `masterpiece`, `dramatic`, `teal and orange`, `volumetric`, `perfect`, and `ultra-detailed`.
- Prefer 35–50 mm, eye-level or modestly handheld framing, ambient practical light, normal skin texture, and realistic exposure roll-off.
- Request a neutral expression or an interrupted action when appropriate; avoid perfect poses, symmetrical framing, and “beautiful sadness.”
- In a series, repeat only the continuity facts (age, hair, clothing, prop, place, time); let each shot's action, framing, and available light vary.
- Add a short negative constraint: `no fashion editorial posing, no glossy skin, no stylized color grade, no artificial fog, no exaggerated tears, no poster-like composition`.

Do not name living artists or imitate a living creator's recognizable style. Translate a requested reference into neutral, observable traits such as controlled symmetry, cool practical lighting, restrained palette, grain, or slow-burn tension.

## Cinematic Decisions

- Let the story beat choose the shot: establishing for isolation or scale; medium for relationship and action; close-up for a decision or private emotion; extreme close-up only for a decisive detail.
- Use lens language sparingly: 24–28 mm for proximity and environmental energy, 35–50 mm for natural perspective, 75–100 mm for compression and intimate separation. Specify a lens only when it serves the frame.
- Motivate light with visible sources: window, neon sign, doorway, phone screen, headlights, sodium-vapor streetlamp, or overcast sky. Describe its direction and effect on the subject.
- Make color purposeful: complementary tension (teal/amber), sickly fluorescent green, desaturated winter blue, dusty earth tones, or a single saturated accent. Avoid default teal-and-orange unless it supports the scene.
- Add texture only when helpful: subtle 35 mm grain, halation around highlights, smoke, rain on glass, imperfect focus falloff, worn production design. Never use grain to hide weak composition.

Read [shot-recipes.md](references/shot-recipes.md) when selecting a genre, framing recipe, realism baseline, or correction for a failed generation. Use its **Rainy platform baseline** for quiet, grounded night exteriors.

## Image Editing

Inspect the supplied image before editing. Preserve identity, pose, geometry, and product details unless explicitly asked to alter them. State the requested change as a precise visual delta, then retain the existing camera perspective and lighting logic where possible.

## Delivery

After generating, show the image without a follow-up summary. Before generation, briefly state the creative direction only when it helps the user verify intent.
