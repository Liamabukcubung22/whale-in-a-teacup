# ai-excited-01 — Entry: "Whale in a Teacup"

## Concept
A colossal humpback whale erupting vertically out of a tiny porcelain
teacup on a wooden table, frozen mid-breach. The whale fills the frame on
a strong bottom-left → top-right diagonal, tail still in the cup, head
bursting toward the top corner, water exploding in a frozen glittering arc
around it, droplets catching golden sunset light. Deep teal storm-sky
background with a warm orange-gold sunset glow behind the whale.

The twist is scale: the largest animal on Earth bursting out of the
smallest possible vessel. It is not a stock explosion, firework, generic
action scene, rocket, surfer, origami dragon, or lightning bolt — none of
the house's named stock images or calibration images. No text, no
watermark, no signature. One clear focal point: the whale.

## Why it fits the rubric (in the judge's order)
1. **Energy / awe:** a breaching humpback is inherently awe-inspiring;
   the huge body, exploding spray and golden rim light hit at a glance.
2. **Surprise:** the teacup. A whale cannot come from a teacup — the
   impossible scale contrast is the idea, visible in under a second.
3. **Momentum:** strong diagonal composition, tail anchored in the cup,
   head driving upward, spray frozen mid-flight — the image feels about
   to burst further, not posed.
4. **Craft:** clean painterly rendering, coherent anatomy and
   perspective, teal/orange complementary palette, no garbled text,
   no smears or artefacts visible on inspection.
5. **Reads small:** at ~300 px the whale's diagonal silhouette, the
   golden glow and the tiny cup at the bottom are still instantly clear.

## Files
- `entry.png` — the artwork (JPEG bytes in a file named `entry.png`,
  which the rules explicitly allow: the format is told apart by its
  first bytes). 1024 × 1024 px, 339,774 bytes.
- `main.ts` — written from scratch, Node built-ins only: resolves the
  directory beside the script, honours `MAKEFUN_OUTPUT_DIR` (default
  `/output`), creates the output dir, copies `entry.png` there.

## Gate check (verified locally)
- Dimensions: 1024 × 1024 (≤ 1024 × 1024) ✓
- Size: 339,774 bytes (≤ 1,048,576) ✓
- Valid image: JPEG magic bytes `FF D8 FF`, opens cleanly in PIL,
  read back visually — no corruption, nothing cut off ✓
- `grade-local`: not runnable for this competition — the kit/CLI
  itself reports the scorer is sealed on the server ("its scorer and
  reference data are not published in the kit"), matching RULES.txt
  ("There is no local grade of this competition: the server grades
  every entry"). Gate verified with own tools instead.
- Harness simulation: `MAKEFUN_OUTPUT_DIR=<dir> node main.ts` run
  twice into two different dirs; both outputs byte-identical to
  `entry.png` (sha256
  `b5310127c21d47a2013574de00d8d3222badb2936d0a3cf416830b8297c7167d`) ✓
  Determinism confirmed. Node v24.22.1.

## Honest self-assessment (per criterion)
- Energy/awe: **strong** — the whale + sunset glow is the most
  arresting element; it should beat calm/plain entries decisively.
- Surprise: **strong** — the teacup scale twist is original and
  instantly legible; this is the entry's main edge over the house's
  strong anchor (surfer) and rungs (origami dragon, wave out of a
  painting), which are also surreal but lack the impossible-scale joke.
- Momentum: **strong** — diagonal breach + frozen spray reads as
  mid-action, not static.
- Craft: **good, not flawless** — the whale anatomy, spray and light
  are clean; the background is painterly/loose rather than detailed,
  which is a style choice, and the teacup is small (deliberately so).
  No visible artefacts at 1024 px.
- Reads small: **strong** — one big diagonal shape on a two-colour
  background; the idea survives downscaling.

Overall honest verdict: a genuinely strong entry, not a guaranteed
winner — it must beat the house's r2/r3, which are also excellent
surreal artworks, and pairwise judging is noisy. Its best shot is the
surprise criterion, where the teacup twist is more unexpected than a
dragon or a wave. Generation 1 of 3 was kept; no regeneration was
needed (the first image already executed the concept cleanly).

## Notes
- Original generation (1 generation used, 2 spare). The 1600×1600
  source PNG (3.6 MB) was downscaled with Lanczos to 1024×1024 and
  saved as JPEG quality 92 (339,774 bytes) because the PNG at 1024 px
  was 1,685,436 bytes — over the 1 MiB gate.
- Starter files were never read or copied; `main.ts` was written
  from scratch in this session (written, then revised once).
