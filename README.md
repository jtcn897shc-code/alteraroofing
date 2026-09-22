# Altera Roof Services website

A static, one-page site for Altera Roof Services (Coquitlam, BC). It's plain HTML, CSS and JS, with no build step.

- `site/`: the deploy folder (`index.html` plus `assets/`). Only this folder ships.
- `review/`: the original client screenshots. Never deployed.
- `docs/DISCOVERY.md`: confirmed facts vs. TODOs. **Read the "blocking launch" list before going live.**
- `docs/DESIGN-PACKAGE.md`: palette, type, hero band map, and every line of copy.
- `.claude/skills/10k-websites/`: the build workflow this site follows.

## Preview
```
cd site && python3 -m http.server 8000
```
Open http://localhost:8000. Opening `index.html` by double-click also works, and shows the still hero.

## Adding the hero film later
1. Encode the approved clip to `site/assets/hero-scrub.mp4`. Extract its first frame to `assets/hero-poster.jpg`. Recipes are in `.claude/skills/10k-websites/references/ffmpeg-recipes.md`.
2. In `site/index.html`, set `VIDEO_READY = true` and `VIDEO_BYTES` to the file's real size.

Fonts: Archivo and IBM Plex Mono, self-hosted under the SIL Open Font License.
