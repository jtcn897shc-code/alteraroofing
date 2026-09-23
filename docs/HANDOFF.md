# Handoff: finishing the hero film

State at the end of the previous session:

- **Site v2 is built** (`site/index.html`): monochrome, Instrument Sans + Space Mono, Andercore-inspired. The hero currently shows the real drone photo `assets/aerial-house.jpg` as a still, because `FILM = false` (in the head script).
- **Start frame is generated** on Higgsfield (2.75 credits spent, ~67 left):
  - job `71b87907-4292-4c1b-a4ef-cae31d1b9f2e`
  - https://d8j0ntlcm91z4.cloudfront.net/user_3FKrk0ewrnItmRz7BhGWUzADkXs/hf_20260922_234409_71b87907-4292-4c1b-a4ef-cae31d1b9f2e.png
  - Neither Claude nor the client has inspected it yet.
- **Blocker:** the session's network policy denied `d8j0ntlcm91z4.cloudfront.net` (403 on CONNECT), so generated files couldn't be downloaded. The client is enabling it in the environment settings.

## Next steps (10k-websites skill, Phase 6 onward)
1. Download the frame to `review/hero-start.png`. Inspect it for logos, text, anatomy and composition, then show the client and get a yes.
2. Preflight (`get_cost:true`) the same 6s 1080p image-to-video shot on 2 to 3 video models. Present the prices against the balance and let the client pick.
3. Prompt: one continuous straight-down descent through the rain mist, with droplets on the lens as it passes the cloud. It ends at rest on a top-down view of the dark roof, ridge centred, rain easing. No text or logos.
4. Video gate: extract frames, save to `review/`, and have the client watch it.
5. Scrub encode it (`references/ffmpeg-recipes.md`) to `site/assets/hero-scrub.mp4`, plus `hero-poster.jpg` and `hero-ending.jpg`.
6. In `site/index.html`, set `FILM = true` and `VIDEO_BYTES` to the real size. Consider swapping `.still` to `hero-ending.jpg` for phones.
7. Self-test (Playwright via `/opt/pw-browsers`), then commit and push.
