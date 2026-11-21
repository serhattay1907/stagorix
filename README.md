# Stariance

AI-powered growth studio for brands and creators: brand profile and packs, content production, publishing and measurement in one place.

| Part | Path | What it is |
| --- | --- | --- |
| Stagorix | [`packages/stagorix`](packages/stagorix) | Open-source video engine (MIT): analysis, edit plan, effects, render |
| Stariance app | [`apps/stariance`](apps/stariance) | Brand wizard, pack recommendation, Insight, panel (from MVP phase E) |
| Docs | [`docs`](docs) | One roadmap and one decision log for the whole repository |

> **Status:** early development. MVP target: 31 December 2026. See the [roadmap](docs/ROADMAP.md).

## Quick start (engine)

```bash
cd packages/stagorix
docker compose up --build        # or: uv sync && uv run stagorix doctor
```

## License

[MIT](LICENSE). Stagorix renders with [Remotion](https://www.remotion.dev), which has its own license; see [`packages/stagorix/README.md`](packages/stagorix/README.md).
