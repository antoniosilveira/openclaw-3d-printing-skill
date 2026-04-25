# OpenClaw 3D Printing Skill

An OpenClaw-native skill for designing **parametric 3D-printable parts** with **CadQuery**.

It helps an agent gather requirements, model physical parts parametrically, export STL or 3MF files, render previews, and iterate on fit, tolerances, and printability.

## What it includes

- `SKILL.md` with trigger and workflow guidance
- `scripts/run_cadquery_model.py` for structured model execution and validation
- `scripts/preview.py` for preview rendering
- `scripts/mesh_io.py` for safe mesh loading
- `scripts/stl_to_3mf.py` for STL to 3MF conversion
- `references/design-review.md` for final review guidance
- `references/requirements.txt` for Python dependency expectations
- `examples/` for small prompt briefs

## Install in OpenClaw

Clone or copy this repository into your OpenClaw skills directory so the repo root itself is the skill folder.

Example:

```bash
git clone https://github.com/antoniosilveira/openclaw-3d-printing-skill.git ~/.openclaw/workspace/skills/openclaw-3d-printing-skill
```

OpenClaw should then discover the root `SKILL.md` automatically.

## Python and CadQuery requirements

This project expects a Python environment that can install CadQuery and the preview stack.

See `references/requirements.txt` for the dependency list.

Typical setup:

```bash
python3.12 -m venv .venv
source .venv/bin/activate
pip install -r references/requirements.txt
```

CadQuery wheel support is best on Python 3.10 to 3.12.

## Packaging the skill

You can validate and package the skill directly from the repo root:

```bash
python3 /path/to/openclaw/skills/skill-creator/scripts/package_skill.py . ./dist
```

That should produce a `.skill` artifact in `dist/`.

## Example usage

See `examples/` for short briefs you can adapt:

- `examples/simple-bracket.md`
- `examples/enclosure-brief.md`

## Attribution

**Inspired by** the original Claude-oriented CAD skill from Flowful:

- [flowful-ai/cad-skill](https://github.com/flowful-ai/cad-skill)

This repository is an **OpenClaw-native adaptation** with its own packaging, layout, and workflow. It is **not an official fork** and is not affiliated with the original project.

## License

MIT. See `LICENSE`.
