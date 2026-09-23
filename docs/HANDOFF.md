# Hero film: shipped

The opening video is live in `site/index.html`: `FILM = true`, real byte size wired in.

## What's in place
- `site/assets/hero-scrub.mp4`: the approved descent (Kling 3.0 std), scrub-encoded (`-g 8 -keyint_min 8`, crf 20, faststart, no audio). 3.47MB, 6s, 1276x720.
- `site/assets/hero-poster.jpg`: first frame, shown while the video streams in.
- `site/assets/hero-ending.jpg`: the resting frame (sharp roof texture), now also the static hero image for phones, reduced motion, and no-JS visitors, replacing the old raw drone photo there.
- Credits spent: 2.75 (start frame) + 9 (first video, rejected, no real motion) + 9 (second video, approved) = 20.75. About 49.33 left on the account.

## One thing worth knowing: this sandbox can't play the video back
Playwright's bundled Chromium here has **no H.264 decoder at all** (`video.canPlayType('video/mp4; codecs="avc1..."')` returns `""` for every profile) — a licensing limitation of open-source Chromium builds, not a problem with the file. Confirmed:
- `ffmpeg -i hero-scrub.mp4 -f null -` decodes it with zero errors.
- `ffprobe` gives a 100% probe score: standard H.264 High Profile, level 3.1, yuv420p, valid faststart moov atom.
- Real Chrome, Edge, Safari and Firefox all ship H.264 support and will play this file normally.

Because of that, every test in this sandbox exercises the **video-missing fallback path** (poster image, then the composed still), which is good — it proves that path thoroughly — but it means **actual scrub playback has not been watched by human eyes yet.** The scroll-driven caption/band logic itself (opacity, `--k`, entrances) was verified directly through the DOM and works correctly regardless of whether the video decodes.

**Next session or the user, please confirm on a real device:** open the live link (or `python3 -m http.server` + the localhost link) in an actual Chrome/Safari/Firefox and scrub the hero at the top, middle and bottom. If it doesn't play there either, something else is wrong and it needs a real look — but every signal so far points to this being sandbox-only.
