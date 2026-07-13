# Contributing

Contributions that make cinematic prompts more specific, grounded, and reusable are welcome.

## Guidelines

- Keep `SKILL.md` focused on the workflow and under 500 lines.
- Put genre-specific or longer examples in `cinematic-visual-generation/references/`.
- Describe observable visual choices: shot size, point of view, light source, location wear, palette, and action.
- Prefer restrained, motivated details over generic quality language such as “masterpiece,” “ultra-detailed,” or “cinematic.”
- Do not add prompts that imitate a living artist’s recognizable style.

## Before opening a pull request

1. Confirm the YAML frontmatter in `SKILL.md` has only `name` and `description`.
2. Ensure paths linked from `SKILL.md` exist.
3. Test a representative request with the skill and revise any vague or conflicting instruction.
4. Keep generated images and temporary outputs out of the change set.
