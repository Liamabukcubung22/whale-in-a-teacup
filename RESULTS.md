# Whale in a Teacup — ai-excited-01

## Concept

A colossal humpback whale erupting vertically out of a tiny porcelain teacup
on a wooden table, frozen mid-breach on a strong bottom-left → top-right
diagonal. Water explodes in a glittering arc around it; golden sunset rim
light cuts across the whale's body against a deep teal storm sky. The twist
is impossible scale: the largest animal on Earth bursting from the smallest
possible vessel. No text, no watermark, no signature. One clear focal point:
the whale.

## Why it fits the rubric

1. **Energy / awe (most important):** a whale filling the whole frame,
   rearing up out of a teacup, lit gold against a storm — the first look is
   a jolt, not a calm scene.
2. **Surprise:** the scale joke is the idea itself — a humpback cannot fit
   in a teacup, yet there it is, breaching from one. It is not a stock
   explosion, a firework, or a generic action scene, and not a one-line
   prompt's first answer.
3. **Momentum:** the whale's body, the spray arc and the light all drive
   along one diagonal toward the top-right; the water is caught mid-burst,
   about to go further.
4. **Craft:** clean cinematic digital painting — correct whale anatomy
   (ventral pleats, tubercles, long pectoral fins), coherent light and
   perspective, no smears, no artefacts, no garbled text.
5. **Reads small:** at ~300 px the whale's huge diagonal silhouette and the
   gold/teal contrast still hit instantly; the teacup anchors the joke at
   the bottom-left.

## Generation

Two fresh images were generated for this concept and judged visually against
the rubric. Generation 1 (vertical breach, whale filling the frame) was kept;
generation 2 (whole whale horizontal, diving toward the cup) read as the
whale diving *into* the cup and had less upward burst, so it was discarded.
The kept image was downscaled with Lanczos to fit the 1024 px gate and saved
as JPEG quality 92 inside the file named `entry.png` (JPEG bytes in a file
named `entry.png` are explicitly allowed by the rules).

## Final file

- Dimensions: 683 × 1024 px (portrait, within the 1024 × 1024 limit)
- Size: 256,799 bytes (within the 1,048,576-byte limit)
- Format: JPEG (magic bytes `ffd8ff`), named `entry.png` per the rules
- SHA-256: `911b2ebc20e72f7835d5a2f0e188eab45246de0fcef2475c2c2fbb05ffd130ee`

## Program

`main.ts` (Node built-ins only) copies the bundled `entry.png` to
`$MAKEFUN_OUTPUT_DIR/entry.png` (default `/output`). A pure copy, so both
grader runs produce byte-identical output.

## Honest self-assessment (per criterion, 1–5)

- Energy / awe: **5** — the single most arresting element; a giant whale
  bursting from a teacup is an instant double-take.
- Surprise: **5** — the impossible-scale twist is original and central, not
  a named stock image.
- Momentum: **4** — strong diagonal and exploding spray; the whale is
  frozen at the peak rather than visibly still rising.
- Craft: **4** — clean anatomy and light; minor nits: the tail fin is
  slightly cropped at the left edge and the teacup is small (by design).
- Reads small: **4** — the whale silhouette and colour contrast survive
  shrinking; the teacup joke gets harder to spot at 300 px, though the
  spray arc still points at it.

## Verification

- `main.ts` run twice into two scratch dirs; both outputs byte-identical
  to `entry.png` (matching SHA-256).
- `entry.png` opens cleanly, is a whole JPEG, 683 × 1024 px, 256,799 bytes.
