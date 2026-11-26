# Study Buddy — Student Beta v0.9

A static, source-based dentistry study platform. The production GitHub Pages branch is `student-beta-v07` (the branch name is retained for existing Pages settings); the application release is v0.9. `main` remains the historical v0.3 branch. The rollback reference for v0.8 is commit `0549b477549440b10d7ea4965b9ee534bd97a1c5`; v0.7 is `8f2e223f29f186736bc3df3b518ea9ae6db201f3`.

## Run

Open the production website at https://terar1kfn.github.io/study-buddy/. For local development, serve the repository root with `python -m http.server 8000`; no build or dependency installation is required for the website. The bundled original lecture photographs and MP4s are relative assets under `assets/images/` and `assets/video/`.

## v0.8 — Daily revision (26 November 2026)

- Today (`#today`): daily goal (5–30 unique rated cards), due/new/future counts, seven-day activity, lecture progress, links to study tools.
- Review (`#review`): all six existing lecture decks, 245 cards. Filter by lab/theory/individual lecture; review due/new or include scheduled cards. Prioritizes previously missed and due cards; intervals: Again 10 minutes, Hard 1 day, Good at least 3 days (up to 30), Easy at least 7 days (up to 60). Rating is self-assessed, not a validated measure of mastery. Individual lesson deck ratings update the scheduler; the legacy mixed-lab deck remains unchanged. New schedule uses the existing `study-buddy-v1` storage key under `state.v8` and does not reset historical data.
- Global search: header button or Ctrl/Cmd+K, source-page results and study-tool shortcuts, keyboard navigation.
- Notebook export now includes the revision schedule and daily activity (JSON schema version 8), along with existing video and study data. Data is local to the browser; export remains one-way, not cloud synchronization or an import feature.
- All existing 150 source pages, 245 flashcards, 101 scored exam questions, 272 image assets, both MP4s, original course structure and interface motion settings retained.

## v0.9 — Memory Lab (26 November 2026)

Open `#memory` from navigation, Today, Study Tools, or any available lesson. Search supports Memory Lab via Ctrl/Cmd+K. Six activities combine evidence-based learning principles with the existing source-backed content:

- Blank-page recall: all 245 existing cards; write or admit a gap before viewing feedback. Self-ratings feed the existing v0.8 scheduler. Retry missed cards; optionally restrict recall to two source pages in a study sprint.
- Mix & distinguish: existing 48 written lab questions, round-robin interleaving across lab topics in all-lectures mode. Confidence recorded before checking; immediate answer feedback, source-page links and retry for errors. High-confidence errors are flagged, not used as a clinical competence measure.
- Teach it back: 13 source-page prompts across all six lectures; compare an explanation with the existing guide and relevant deeper explanation. Optional saved text and self-check rubric. No automated grading.
- Photo recall: existing 53 lab photographs; retrieve the name and purpose, then reveal. Some original packaging has labels; this is not a blinded exam.
- Memory palace: five editable cue routes (21 stations), based on sealant, processing waxes, capsule instruments, alginate and two-step impression. Recall walk hides mnemonic and facts until reveal. Mnemonic cues are optional, not clinical guidance. Evidence for loci is lower certainty than spacing/retrieval.
- Study sprint: 10, 20 or 30 minute *suggested* plans, source links, focused recall and a local checklist. No claim that these durations are optimal; not a timer or automatic time tracker.

Seven linked scholarly sources on the hub explain the evidence and limitations. No new source lecture content or assets are added. State lives under `state.v9` in `study-buddy-v1` (last 500 responses, saved explanations, personal cues and current sprint); notebook export schema 9 includes Memory Lab and existing data. No network submission, AI grading, or account sync. Study Buddy's new activities themselves have not been experimentally validated.

## Verification

v0.9: Node syntax checks and isolated Chromium tests covering all six new activities, scheduler integration, cross-topic ordering, source feedback, saved explanations/cues, sprint persistence, quick search, existing routes, question counts, and responsive layouts at 360/390/768/1440 px. Test-only storage shim used, so true browser persistence remains unverified.

Earlier v0.8: Node syntax checks for added and changed JS; isolated Chromium test of 17 application routes, daily goal, five-card session, legacy rating integration, serialized progress, search-to-source navigation, and representative routes at 360/390/768/1440 px. No script errors in that test. Normal HTTP navigation is blocked by the test environment, so browser tests used inline copies of the exact sources and a test-only storage shim. Real browser reload persistence and live student-device playback should be checked after deployment. The 28-second cinematic V2 is a preview, not the full film.

## Source and privacy policy

Preserve full lecture explanations, source-page references, material-specific figures and explicitly identified discrepancies. Models are conceptual rather than clinical simulations. No official exam claims. Course materials and film assets are intended for educational use; public GitHub Pages distribution requires the relevant rights. No student analytics or personal information is sent to a server by the revision feature. Progress is saved on the current device.
