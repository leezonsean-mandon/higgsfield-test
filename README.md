# Soul Studio

A chat-driven ad studio: **you as the model, any clothing brand on the rack.**
Campaigns are briefed in a Claude chat (phone or desktop), generated on
[Higgsfield](https://higgsfield.ai), and delivered to one private gallery page.

**Gallery:** https://claude.ai/code/artifact/b9bfa246-66e0-4b77-9b58-ea5880fcd9cb

## How it works

There is no app to operate. The chat is the control surface; this repo is the
system of record; the gallery is the shop window.

```
chat brief ──► shot package + credit quote ──► approval ──► Higgsfield generation
                                                                │
                        gallery page + manifest.json  ◄── QC (likeness + garment fidelity)
```

### 1. Avatar setup (one time)

Drop **10–20 photos of yourself** in the chat:

- 5+ face close-ups — varied angles, expressions, lighting
- 3+ waist-up shots
- 2+ full-body shots (try-on videos need your build, not just your face)
- Recent, unfiltered, no beauty smoothing; solo frames only; face unobstructed
  (no sunglasses/heavy shadows) in most shots. Phone camera is fine.

A small calibration batch follows (quoted first): a few test stills, you pick
the truest 1–2, and that likeness is locked as the reference for every future
campaign. Locked identity details (character/reference IDs) are recorded in
`campaigns/manifest.json` under `avatar`.

### 2. Campaign brief

One message in chat:

| Field    | What to send                                                        |
| -------- | ------------------------------------------------------------------- |
| Garment  | Product photos (flat-lay/packshot/model shot) **or** a product URL   |
| Vibe     | One line — e.g. "quiet luxury, overcast rooftop, film grain"         |
| Formats  | Optional — defaults below apply if unstated                          |
| Notes    | Optional — scenes to include/avoid, references, copy to overlay      |

### 3. Quote → approve → deliver

Every campaign gets a proposed shot package and a **credit quote before
anything generates** (standing policy: quote-before-batch). After approval,
assets render, pass QC, and land in the gallery with download links. Nothing
is ever auto-posted to any social platform.

## Formats & defaults

| Format             | What it is                                                     | Default   |
| ------------------ | -------------------------------------------------------------- | --------- |
| Photo ad set       | Editorial stills — hero + 3–5 alternate scenes/angles           | ✅ on     |
| Cinematic video ad | 5–10s motion ad from the best stills, with soundtrack + clean   | on request|
| Try-on / fit video | UGC-style fit check via Higgsfield's dedicated try-on workflow  | on request|

- **Aspect ratio:** 9:16 vertical everywhere (reframes to 4:5 / 16:9 on request)
- **Publishing:** manual — gallery + downloads only
- **Credits:** balance at setup 797.5 (Plus plan); every batch is quoted first

## Repo layout

```
README.md                 — this manual
campaigns/manifest.json   — machine-readable registry: avatar identity, defaults,
                            one entry per campaign (brief, quote, asset URLs, status)
gallery/index.html        — source of the gallery page (published as a Claude artifact;
                            republishing this file updates the same URL)
```

Campaign lifecycle: `briefed → quoted → generating → qc → delivered`.
Each delivered campaign appends an entry to the manifest and a card to the
gallery, then both are committed here — the repo always rebuilds the gallery.

## Note on brand imagery

Product photos and brand names are supplied by the studio owner. For client or
commercial work, make sure you're licensed to use the brand's product imagery.
