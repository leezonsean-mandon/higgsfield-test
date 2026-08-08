# Soul Studio — resume state (2026-08-08, session 2)

## Done
- All 20 avatar refs ingested into Higgsfield as confirmed media_ids
  (map in campaigns/manifest.json `avatar.reference_media_files`).
  Route: this session's egress policy blocked upload.higgsfield.ai
  (allowlist change hadn't propagated), so Mandon approved a brief
  public-repo window and the refs were imported server-side via
  media_import_url from commit-pinned raw URLs. Repo is back to private.
- Soul character **"Mandon"** (type soul_2) **TRAINED and ready** (14:47Z →
  15:12Z) on all 20 refs — soul_id `4a99edd9-e70a-4a3f-98cf-e758dc53f038`.
  Training fee: 25 credits (flat "Soul ID" charge; balance now 772.5).
- Calibration batch quoted from a get_cost preflight (no jobs submitted):
  Soul 2.0 still 9:16 2k = **0.12 credits exact** → 6-still batch ≈ **0.72
  credits**. Delivered to Mandon; awaiting his approval (quote-before-batch).
- Gallery artifact updated (same URL, in manifest `gallery_url`).

## LIKENESS ISSUE — investigation state (16:05Z)
Mandon: calibration stills "not even close". Verified so far:
- Refs are correct + consistent (4 viewed) with minor IG chrome overlays.
- Training media on Higgsfield CDN byte-identical to repo files.
- soul_id validated server-side (fake id → "Character not found"); real jobs
  resolve to character "Mandon".
- Every Soul V2 job gets style "General" @ strength 1 injected server-side;
  MCP rejects style_strength override ("not supported").
Diagnostics generated (0.24 cr): test A soul-only re-run
(hf_..._160029_8394f73f...), test B soul + direct photo reference 7107
(hf_..._160357_1f1381d8...). Balance 771.54.
DECISIVE CROSS-CHECK (Mandon, free): generate the same portrait from
character "Mandon" in the Higgsfield WEB app (style off/none if possible).
Web likeness good → MCP generation path defect (report to Higgsfield; use
soul+photo-reference or web meanwhile). Web also bad → training weak →
retrain (25 cr, needs approval) on cleaned refs (crop IG chrome; better:
original camera photos, not screenshots).

## NEXT STEP (after cross-check)
1. Resolve likeness per above, re-run calibration, Mandon picks 1–2 → lock.
2. Then first campaign brief (garment photos/URL + vibe) → package + quote →
   approval → generate → gallery + manifest.
NOTE: repo still public at last check — confirm Mandon wants it flipped back.

Standing decisions: 9:16 default, formats photo_set/cinematic_video/try_on_video,
manual publishing only, quote before every batch. Balance 772.5 (Plus);
session spend: 25 credits (Soul ID training fee only — imports and cost
preflights were free).
