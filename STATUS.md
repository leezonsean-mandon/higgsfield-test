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

## NEXT STEP
1. On Mandon's calibration approval: 6× Soul 2.0 stills, 9:16, 2k, varied
   scenes (portrait / editorial waist-up / full-body street / profile /
   low-light cinematic / natural-light candid) via generate_image_batch with
   soul_id, then jobs_wait, then ONE show_generation_by_ids. Mandon picks the
   truest 1–2 → record picks + locked_at in manifest, refresh gallery.
2. Then first campaign brief (garment photos/URL + vibe) → package + quote →
   approval → generate → gallery + manifest.

Standing decisions: 9:16 default, formats photo_set/cinematic_video/try_on_video,
manual publishing only, quote before every batch. Balance 772.5 (Plus);
session spend: 25 credits (Soul ID training fee only — imports and cost
preflights were free).
