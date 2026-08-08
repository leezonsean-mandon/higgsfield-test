# Soul Studio — resume state (2026-08-08)

Everything below is DONE:
- Studio scaffold: README.md (playbook), campaigns/manifest.json, gallery/index.html
- Gallery artifact live: https://claude.ai/code/artifact/b9bfa246-66e0-4b77-9b58-ea5880fcd9cb
- 20 avatar reference crops curated + verified: avatar/refs/*.jpg (IG chrome removed)
- Environment network allowlist updated by Mandon: upload.higgsfield.ai, d2ol7oe51mr4n9.cloudfront.net
  (applies to sessions created AFTER the change)

NEXT STEP (blocked in the old session by pre-change network policy):
1. Verify container can reach https://upload.higgsfield.ai (HTTP code, not CONNECT 403)
2. Higgsfield media_upload: 20 slots -> curl PUT each avatar/refs/*.jpg -> media_confirm (type image)
3. show_characters action=train, name "Mandon", type soul_2, images=[20 media_ids] (~10 min)
4. QUOTE the calibration batch BEFORE generating (standing policy: quote-before-batch):
   ~6 Soul V2 stills, 9:16, varied scenes; Mandon picks truest 1-2 as locked look
5. Record soul_id + calibration picks in campaigns/manifest.json avatar block
6. Then first campaign brief (garment photos/URL + vibe) -> package + quote -> generate ->
   update gallery artifact (pass url param to update the same artifact) + manifest

Standing decisions: 9:16 default, formats photo_set/cinematic_video/try_on_video,
manual publishing only, quote before every batch. Balance at setup: 797.5 (Plus).
