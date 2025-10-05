# Nuke Launchpad v1.0.0

Nuke Launchpad is a drop-in starter kit for building adaptive, production-ready AI features with Apple Intelligence.

It’s more than sample code — it’s a system-native architecture that shows how to:
	•	✨ Integrate Foundation Models for guided, typed generation
	•	🧩 Expose AI features through App Intents & Spotlight
	•	🛡 Keep all processing private and on-device
	•	⚡️ Optimize performance with thermal/battery-aware auto-tuning
	•	📊 Monitor with os_signpost / Logger metrics & Policy Inspector UI
	•	♻️ Persist learning across launches for a self-optimizing experience

Everything is engineered to feel like a first-party Apple feature: efficient, privacy-first, and adaptive.

⸻

## What’s Inside

| Pack                       | Purpose                                                                                       |
|----------------------------|-----------------------------------------------------------------------------------------------|
| core-demo.zip              | Minimal App Intent + Foundation Models + tool-calling demo                                   |
| additive-pack.zip          | Shortcut importer, privacy sanitizer, Spotlight delegate                                      |
| additions-v2.zip           | Gallery-ready Shortcut JSON, privacy toggle, scheduler                                       |
| final-touches.zip          | BG tasks, caching, gallery metadata                                                           |
| observability-bg-charging.zip | os_signpost / Logger metrics + charging-aware background tasks                               |
| autotuner-inspector.zip    | Contextual Thompson Sampling + Policy Inspector UI                                            |
| bandit-persistence.zip     | Crash-safe JSON persistence for α/β posteriors                                               |
| final-glue-code.zip        | AppLifecycle heartbeat, rollout flags, bootstrap seeding                                      |

⸻

## Privacy First
	•	🔒 All summarization and tuning runs on device.
	•	🧹 Optional NER-based redaction to keep PII out of Spotlight.
	•	✅ Checksums included so developers can verify every asset.

⸻

## Quickstart

# Download all release assets (requires GitHub CLI)
gh release download v1.0.0 -R jsonwisdom/nuke-launchpad --pattern "*.zip"

# Verify integrity
shasum -a 256 *.zip | diff - SHA256SUMS.txt

Open the core-demo project in Xcode 15+/iOS 18/macOS 15, run on device, and try:
	•	Spotlight → “Summarize Note” → see adaptive snippet
	•	Tap Create all reminders to test tool-calling
	•	Use Policy Inspector to watch the auto-tuner learn in real time

⸻

## Next Steps for Contributors

We’d love to see Nuke Launchpad grow into the go-to starter kit for Apple-native AI apps.

Ways you can help:
	•	🧩 Feature Ideas & Requests – Open an issue to propose new packs (e.g., alternate tool-calling flows, richer Spotlight snippets, multi-model adapters).
	•	🐞 Bug Reports & Fixes – File issues or PRs if you spot edge cases (latency handling, thermal heuristics, caching bugs).
	•	⚙️ Tuning Research – Contribute experiments: new bandit arms, alternate decay models, Bayesian optimization upgrades.
	•	🛠 Platform Expansions – macOS menu bar helpers, vision-based summarization examples, additional App Intents.
	•	📝 Docs & Demos – Better quickstarts, videos, sample projects.

Fork → branch → PR. Please keep commits clear and reference any related issues.
Before submitting, run the included unit tests (SafetyTests, AutoTunerTests) to ensure regressions are caught.

If you plan a significant architectural change, open a discussion first so we can align.

⸻

## License

MIT License — use freely in personal or commercial apps.

⸻

This is now a single file you can drop straight into your repo and paste into the GitHub release creation screen.