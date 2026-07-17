# Changelog

What's shipped, and roughly when - grouped by the order features actually landed, referenced against the commit that shipped each batch.

## 1.2.0 - current
- **Auto-update**: TRACE now checks this repo's Releases on launch and can download/install a newer version itself, asking before each step.

## 1.1.0 (`05b3739`)
- **A/B testing**: its own panel and creation flow, variants on any screen in the flow (not just the entry point), a side-by-side comparison view, and a cross-variant AI analysis.
- Fixed the AI analysis misreading internal click-tracking shorthand (`"(background)"`, `"(overlay backdrop)"`) as if it named an actual UI element that appeared, rather than describing where a miss-click landed.

## 1.0.0 (`e35e7fb`)
- AI trend analysis compares testers by their pre-test questionnaire answers (age, occupation, or any custom question) against their outcomes, calling out which group struggled more - with a guardrail against over-reading a one- or two-session sample.
- README documents exactly what data gets sent to the AI and which provider endpoint is used.

## 0.4.0 - First Click testing & AI trend analysis (`c6d794b`)
- **First Click mode**: a heatmap and ranking of where testers click *first* on a screen, not everything they click.
- **AI trend analysis**: summarizes friction points and trends from a test's sessions via Anthropic (Claude), OpenAI (GPT), Google (Gemini), or a private/local model (e.g. Ollama) - free and offline with the local option.
- Dedicated "AI Insights" and "First Click" sidebar entries, each jumping straight to a chosen test.

## 0.3.0 - Light theme redesign & aggregate heatmap (`e844364`)
- Off-white light theme with box shadows and a new blue accent, set as the default (dark mode became opt-in).
- **Aggregate average heatmap** mode, showing what fraction of *all* testers clicked each spot, with its own download option.
- Import moved from the sidebar to a button on the Tests page.
- Dataset export switched from JSON to plain text.

## 0.2.0 - Settings, theming, and sidebar redesign (`84494b1`)
- Settings page: light/dark toggle, saved Figma personal access token, app version/author/GitHub link.
- Persistent left-hand sidebar that scales with window size.
- UI polish: icons, spacing, an animated settings gear.

## 0.1.0 - Baseline
- Import prototypes from Figma, host them for testing, and record click/tap/movement telemetry.
- Per-test click/movement heatmap, success/time/click stats, and a session log.
- Pre-test questionnaire (custom + quick-toggle demographic questions) and an optional post-test comment box.
- Run locally, or share a remote link.
