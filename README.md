# Tulip Bloom

A tulip that grows itself in the browser — the stem draws like a pen stroke, leaves
unfurl, and the petals open from a closed bud. Then it sways, quietly, forever.

Pure SVG + CSS animation. No build step, no dependencies, one file.

## Run it

Open `index.html` in any browser. That's it.

```bash
git clone https://github.com/immortal71/birthday-gift
cd birthday-gift
open index.html        # macOS  (use `xdg-open` on Linux, `start` on Windows)
```

To serve it locally instead:

```bash
python3 -m http.server 8000
# then visit http://127.0.0.1:8000
```

## Publish it

Settings → Pages → Deploy from branch → `main` / root. It'll be live at
`https://immortal71.github.io/birthday-gift/`.

## Timing

The whole sequence runs about 5 seconds:

| Time  | What happens              |
|-------|---------------------------|
| 0.35s | stem draws upward         |
| 1.45s | leaves unfurl, one by one |
| 1.95s | side branch and its bud   |
| 2.55s | petals open in waves      |
| 3.70s | stamens fade in           |
| 4.60s | caption appears           |

Tweak any of it in the `animation-delay` values at the top of the `<style>` block.
Petal colors live in the `<defs>` gradients — `gDark`, `gMid`, `gLight`.
