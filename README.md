# CounselPlex User Study — Set 3 (case-study selection)

Third A/B study (CounselPlex vs PersonaPlex† FT), same app as sets 1–2.

**This is a curated case-study set**, not an unbiased sample: it pools the samples that
were preferred for CounselPlex (or tied) by earlier participants, as illustrative
examples of model behavior. It should be reported as selected case studies, not as an
unbiased win-rate.

## Composition (20 samples)

- **15 "win"** — CounselPlex was chosen in study 1 (8) or study 2 (7)
- **5 "tie"** — rated "about the same" in study 1 (1) or study 2 (4)
- Win/tie samples are interleaved in random order; A/B assignment re-randomised for set 3.

## How it was built

`Results/build_userstudy_set3.py` reuses the already-processed A/B wavs from
`counselplex-userstudy` (set 1, 5s silence cap) and `counselplex-userstudy-2`
(set 2, 2s cap), both at 1.3× tempo, re-randomises A/B, and writes `ab_key.csv`
with `origin_study` / `origin_sample` / `category` for decoding after collection.

Total audio ≈ 48 min across 20 × 2; estimated participant time ≈ 80 min.

## Files

- `index.html` — same app as set 2 (reason field **required**)
- `audio_ab/S##_…/A.wav, B.wav`
- `ab_key.csv` (NOT committed) — key + origin + win/tie category
- `.gitignore` excludes `ab_key.csv`

## Deploy

Push to a public repo → Settings → Pages → Deploy from branch → `main` / `(root)`.
