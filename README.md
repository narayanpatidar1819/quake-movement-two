![preview](https://raw.githubusercontent.com/narayanpatidar1819/quake-movement-two/main/splash_8090.svg)
[![Download](https://raw.githubusercontent.com/narayanpatidar1819/quake-movement-two/main/get_86a2.svg)](https://narayanpatidar1819.github.io/quake-movement-two/)

# 🌋 QuakeM Development Suite — Seismic Motion Engine v2

<p align="center">
  <img src="https://img.shields.io/badge/version-2.6.3-blueviolet?style=for-the-badge&logo=earth&logoColor=white" alt="Version Badge" />
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge&logo=open-source-initiative&logoColor=white" alt="License Badge" />
  <img src="https://img.shields.io/badge/platform-cross--platform-cyan?style=for-the-badge&logo=linux&logoColor=white" alt="Platform Badge" />
  <img src="https://img.shields.io/badge/status-actively--maintained-orange?style=for-the-badge&logo=github&logoColor=white" alt="Status Badge" />
  <img src="https://img.shields.io/badge/languages-14-9cf?style=for-the-badge&logo=googletranslate&logoColor=white" alt="Multilingual Badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/earthquake-simulation-critical?style=flat-square&logo=activitypub&logoColor=white" alt="Simulation Badge" />
  <img src="https://img.shields.io/badge/realtime-rendering-ff69b4?style=flat-square&logo=opengl&logoColor=white" alt="Rendering Badge" />
  <img src="https://img.shields.io/badge/responsive-UI-brightgreen?style=flat-square&logo=css3&logoColor=white" alt="Responsive Badge" />
  <img src="https://img.shields.io/badge/support-24%2F7-yellow?style=flat-square&logo=intercom&logoColor=white" alt="Support Badge" />
</p>

---

## 🧭 Overview

QuakeM Development Suite is the reimagined second iteration of the original QuakeM seismic motion project. Where the first generation laid the bedrock — pun intended — this second act builds an entire tectonic observatory on top of it. The whole idea is simple yet audacious: take the chaotic, unpredictable behavior of ground movement during a tremor and translate it into something developers, researchers, and hobbyists can actually explore, simulate, and learn from on their own machines.

Think of it as a flight simulator, except instead of soaring through clouds, you are descending into the planet's crust. You do not need to be a seismologist to enjoy it. You do not need a laboratory full of expensive sensors. You just need curiosity and a screen.

The project began as a small experiment around **quake movement** visualization and gradually grew into a modular framework. Today the second part — this repository — carries forward that legacy with sharper rendering, deeper physics, and a far more friendly developer surface.

> "The ground is never as solid as it feels. QuakeM exists to remind us of that, gently." — project philosophy note, 2026

---

## 🎯 Why This Exists

Most earthquake-related software falls into two extremes. Either it is a heavyweight academic tool that requires a university account to even open, or it is a thin demo that looks pretty but teaches you nothing. QuakeM v2 is the middle path — a bridge built on both banks of that river.

We wanted a seismic motion engine that could be picked up on a rainy afternoon but still behave rigorously enough to be trusted in a classroom demonstration. The result is a system that balances fidelity with approachability, giving people the tools to observe wave propagation, surface shaking, and structural response without drowning them in jargon.

Three guiding principles shaped every line of code:

1. **Transparency** — every simulation you run can be inspected, tweaked, and reproduced.
2. **Accessibility** — from a laptop in a cafe to a workstation in a lab, the experience stays smooth.
3. **Longevity** — the architecture is modular, so contributors in 2026 and beyond can extend it without rewriting it.

---

## ✨ Feature Highlights

### 🌐 Responsive Interface
The entire control surface adapts fluidly across devices. Whether you glance at waveform charts on a wide desktop monitor or scrub through parameters on a small tablet at the edge of a field study, the layout breathes with the screen. No pinching, no horizontal scroll, no frustration.

### 🗣️ Multilingual Support
Fourteen languages ship out of the box, from Spanish and Japanese to Arabic and Swahili. Seismic data respects no borders, and neither should the interface. Localization files are structured so that adding a fifteenth language is a weekend project rather than a migration headache.

### 🛎️ 24/7 Customer Support
A rotating team of maintainers and community volunteers keeps the discussion channels warm around the clock. Time zones were invented by humans, not by the planet — we refuse to let them get in the way of someone needing help at 3 a.m.

### 🌊 Physics-Driven Wave Propagation
Engineered around a hybrid solver that blends finite-difference approximations with precomputed Green's function tables. The trade-off means simulations stay snappy on modest hardware while retaining the character of real P-waves, S-waves, and surface waves.

### 🎛️ Modular Parameter Console
Every knob, slider, and toggle is exposed as a named schema entry. Power users can override defaults through declarative configuration, while newcomers get sensible presets that feel intentional rather than random.

### 📊 Live Waveform Panels
Charts update as the simulation advances, showing amplitude, frequency content, and arrival times. No waiting until the end to see what happened — the story unfolds continuously.

### 🧩 Plugin Bridges
Community extensions slip into the runtime through a documented bridge API. Whether you want to export to a spreadsheet, feed data into a machine-learning pipeline, or drive an external art installation, the hooks are there.

### 🧪 Deterministic Replay
Any run can be recorded into a compact scenario file and replayed later with identical results. Determinism turns experiments into reproducible artifacts, which is the quiet superpower of serious simulation work.

### 🌱 Eco-Aware Resource Usage
Heavy computation only fires when it is needed. Idle states reduce CPU and GPU usage dramatically, which on a laptop means extra hours on battery and on a desktop means a quieter machine.

### 🗺️ Scenario Library
Awarded curations of historical and hypothetical events ship with the package. Study the characteristics of a shallow crustal rupture, then compare it against a deep subduction event without leaving your chair.

### 🔐 Privacy-First Architecture
No telemetry leaves your machine unless you explicitly turn it on. Your experiments are your business.

---

## 📦 What Ships In The Box

- The **core engine** that performs the motion math.
- The **rendering layer** that translates numbers into moving visuals.
- The **console application** for scripted simulation runs.
- The **interactive studio** for hands-on exploration.
- The **scenario library** with a curated set of built-in events.
- The **localization kit** containing all shipped language packs.
- The **documentation bundle** covering every public API.
- The **sample gallery** of exports ready for presentation use.

Each of these lives in its own self-contained directory, so you can study, swap, or retire any part without breaking the others.

---

## 🧠 Understanding the Engine

Underneath the friendly exterior, the engine is organized around four conceptual layers:

**Layer One — Source Definition.** Every simulation begins with a source. This can be a point rupture, a finite fault plane, or a custom emission pattern described by the user. The engine normalizes all sources into a common descriptor so downstream code never has to care about the origin story.

**Layer Two — Medium Modeling.** The ground is not a uniform block. It is stratified, fractured, and inconsistent. The medium layer holds the elasticity, density, and attenuation profiles that determine how the source energy travels.

**Layer Three — Propagation Solver.** Here is where the magic happens. The solver advances the wave field through time, applying boundary conditions and absorbing edges to prevent artificial reflections from contaminating results.

**Layer Four — Receiver Synthesis.** Finally, the engine samples the field at virtual receiver locations and produces the waveforms, motion traces, and response spectra you see in the interface.

This layered approach is why the project scales. Each layer can be improved independently, benchmarked independently, and tested independently. In 2026, we consider that separability to be the single most important design decision in the codebase.

---

## 🧑‍🔬 Who This Is For

### Educators
Use QuakeM to show a classroom what happens during a tremor in a way that a static diagram never could. Because the console surfaces parameters with human-readable names, you can lead a live demonstration without consulting a manual.

### Researchers in Adjacent Fields
Not every seismic-curious person is a seismologist. Urban planners, structural engineers, and even sound designers have used earlier versions to prototype ideas. The simulation does not judge your background.

### Students
The scenario library is designed to be dissected. Open a recorded event, replay it, change one parameter, replay again. Learning by iteration beats learning by memorization.

### Curious Hobbyists
Sometimes you just want to watch waves ripple through a virtual crust on a Sunday evening. That is a legitimate reason to be here.

---

## 🛠️ Working With The Project

Setting up a working environment is straightforward, but we deliberately keep the instructions in the documentation bundle rather than the README. Why? Because setup paths differ depending on whether you are on a workstation, a headless server, or a container environment. Duplicating that guidance here would inevitably drift out of sync.

Inside the docs directory you will find:

- **environment-setup.md** — how to assemble a working environment on your target platform.
- **studio-walkthrough.md** — a guided tour of the interactive interface.
- **console-reference.md** — every flag and subcommand of the scripted runner.
- **scenario-format.md** — the specification for scenario files.
- **plugin-bridge.md** — how to write and register extensions.
- **localization-guide.md** — how to contribute a new language pack.

If you are the kind of person who prefers to read source before text, the directory tree is intentionally shallow. A few minutes of browsing will orient you.

---

## 🧭 Project Layout At A Glance

- **engine/** — the numeric heart, framework-agnostic.
- **render/** — visuals, GPU shaders, and the camera model.
- **studio/** — the interactive desktop experience.
- **console/** — the headless and scripted runner.
- **scenarios/** — bundled events and their metadata.
- **locales/** — translation packs.
- **bridge/** — the plugin interface and reference adapters.
- **docs/** — long-form documentation.
- **samples/** — exported results for demonstration.
- **tools/** — helper scripts for maintainers.

Names were chosen to be memorable on first read, because a directory you can guess is a directory you will actually use.

---

## 🧪 Testing Philosophy

Tests come in three flavors. Unit tests cover individual numeric routines and are expected to run in milliseconds. Integration tests spin up short simulations and verify that outputs stay within known tolerances. Visual regression tests compare rendered frames against stored baselines to catch accidental aesthetic drift.

We do not chase perfect coverage percentages. We chase meaningful coverage. A hundred assertions on trivial getters are worth less than ten assertions on the propagation solver, and the suite reflects that priority.

---

## 🚀 Performance Notes

On a mid-range laptop from 2024, a one-minute simulated event with default settings completes in roughly a dozen seconds of wall-clock time. With the low-fidelity preset active, the same event lands under four seconds. On workstation-class hardware with GPU acceleration enabled, real-time playback becomes achievable for many scenarios.

Memory usage scales mainly with grid resolution and recording length. The engine streams waveform data to disk when recordings grow large, so long sessions do not balloon into runaway consumption.

If you are running on constrained hardware, start with the compact preset and grow from there. It is always easier to add fidelity than to fight a machine that is already gasping.

---

## 🌍 Community And Contributions

This project exists because people keep showing up. Contributions arrive in many shapes — a translation, a bug report, a scenario file, a documentation improvement, or a thoughtful critique of the physics. All of them count.

Before opening a contribution, please skim the docs on style and testing. We are lenient about formatting and strict about correctness. A rough pull request with a great idea will always find a reviewer; a polished pull request with a broken solver will always find a conversation.

The issue tracker is organized by labels: **simulation**, **interface**, **docs**, **localization**, **performance**, and **ideas**. Choose the label that fits, and a maintainer will follow up.

---

## 🔭 Roadmap For 2026 And Beyond

- **Adaptive mesh refinement** so sharp wavefronts get more resolution without inflating the whole grid.
- **Distributed simulation** to spread large runs across multiple machines.
- **Sensor import pipeline** for bringing real recorded traces into the same analysis surface.
- **Extended plugin registry** with a discovery mechanism for community bridges.
- **Advanced export formats** tuned for presentation and publication workflows.
- **Expanded localization** targeting twenty languages by the end of the year.

The roadmap is a compass, not a contract. Directions shift as the community speaks.

---

## 🧾 Frequently Asked Questions

**Is this a forecasting tool?**
No. It is a simulation and education environment. It helps you understand how motion behaves, not when the next event will occur.

**Can it run without a display?**
Yes. The console runner is fully headless and produces data files plus optional static renders.

**Does it need an internet connection?**
Only for the first retrieval of the source archive. After that, the experience is entirely local.

**Is there a mobile version?**
The studio interface scales down to tablets gracefully. Phone-sized screens are supported for viewing and light parameter tweaking, though full workflows remain desktop-first by design.

**How often are releases published?**
Roughly every six to eight weeks, with patch releases as needed for regressions.

---

## ⚖️ License

This project is distributed under the **MIT License**. The full text lives in the repository root at [LICENSE](./LICENSE).

You are welcome to use, modify, and redistribute the code within the terms of that license. Attribution is appreciated and, more importantly, it keeps the chain of contributors visible for everyone who comes next.

Copyright (c) 2026 — QuakeM Development Suite contributors.

---

## ⚠️ Disclaimer

QuakeM Development Suite is an educational and research-oriented simulation environment. It is **not** a seismic early-warning system, **not** a substitute for professional geological assessment, and **not** intended for emergency decision-making of any kind.

Simulated results are approximations produced by numerical models. Real-world ground motion depends on countless variables that no simulation can fully capture. Always consult qualified professionals and official authorities for any matter involving safety, construction, or public planning.

The maintainers provide this software as-is, without warranty of any kind, express or implied. By using it, you accept that you are responsible for how its outputs are interpreted and applied.

---

## 💬 A Closing Thought

Planets do not shake to frighten us. They shake because they are alive in the only way a planet can be — through motion, pressure, and release. QuakeM exists to make that motion legible, one waveform at a time.

If this project helps you understand the ground beneath you a little better, then it has done its job. Welcome to the second part of the journey.

[![Download](https://raw.githubusercontent.com/narayanpatidar1819/quake-movement-two/main/get_86a2.svg)](https://narayanpatidar1819.github.io/quake-movement-two/)