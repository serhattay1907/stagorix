# AGENTS.md — Stariance monorepo

Stariance is an AI-powered growth studio for brands and creators: research, packs, content production, publishing and measurement. Stagorix is its open-source video engine. Both live here.

## Layout
- `packages/stagorix/`: video engine (MIT). Python 3.12 + uv, Remotion in `render/`, Docker.
- `apps/stariance/`: app layer (brand wizard, pack recommendation, plan approval, preview, Insight, panel). Built in MVP phase E.
- `docs/`: source of truth. Read `ROADMAP.md` ("Stariance MVP alignment") and `DECISIONS.md` first, then `ARCHITECTURE.md`, `MOTION.md`, `CONTRIBUTING.md`.

## Product model
- Brand profile: personality (Aaker's five dimensions) → style → pack. The format (narrative structure) is chosen per video. Identity can change later: versioned, undoable, repositioning shown as a gradual plan.
- Pack recommendation: top 3 by fit score, "show all" always available.
- MVP outputs: video 9:16 + 16:9, cover image, text (title, description, hashtags). Target: 31 Dec 2026.

## Principles
1. Brand-agnostic: brands only configure it; never hard-code a brand, channel or person.
2. Packs shape how content looks, never what it says. Freedom of content.
3. Same result on macOS, Windows and Linux; the golden test (`stagorix verify`) guards it.
4. User control: every step visible, nothing publishes without approval, everything undoable.
5. Quality over quantity: fewer, crafted effects, sounds and fonts; premium, calm UI.
6. Model-agnostic: every LLM call goes through one adapter interface (Claude first).
7. The engine must not import from `apps/`; the app uses the engine through its CLI/API only.

## Workflow
- One branch per task; the owner merges into `main`.
- Before finishing, in `packages/stagorix/`: `uv run ruff check .`, `uv run ruff format --check .`, `uv run pytest`; in `packages/stagorix/render/`: `npm run typecheck`.
- Record decisions in `docs/DECISIONS.md` (newest first) and progress in `docs/ROADMAP.md`.
- Only permissively licensed dependencies and assets; log every license.
- Code, docs and commits in English. No AI attribution in commits, PRs, docs or code.
