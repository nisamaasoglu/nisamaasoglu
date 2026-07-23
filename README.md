<img src="docs/banner.svg" alt="Nisa Maaşoğlu — Software Engineer" width="100%">

<p align="center">
  <a href="https://linkedin.com/in/nisamaasoglu"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:nisamaasoglu7@gmail.com"><img src="https://img.shields.io/badge/Email-0E1A22?style=flat-square&logo=gmail&logoColor=43D9C4" alt="Email"></a>
  <img src="https://img.shields.io/badge/open%20to-software%20engineering%20roles-43D9C4?style=flat-square" alt="Open to work">
</p>

I build systems where a live signal has to become a decision: a microphone, an electrode, a
camera frame, a retrieved paragraph. The sensor is never the interesting part. The
interesting part is what you are allowed to conclude from it, and how the system behaves
when the honest answer is *not yet*.

---

## Running right now

Not screenshots. These are the actual pipelines, recorded live.

<table>
<tr>
<td width="33%" valign="top">
  <a href="https://github.com/nisamaasoglu/Aurora"><img src="https://raw.githubusercontent.com/nisamaasoglu/Aurora/main/docs/images/aurora_live.gif" width="100%" alt="Aurora — audio driving a volumetric shader"></a>
</td>
<td width="33%" valign="top">
  <a href="https://github.com/nisamaasoglu/LetheFS"><img src="https://raw.githubusercontent.com/nisamaasoglu/LetheFS/main/docs/demo.gif" width="100%" alt="LetheFS — files decaying into quarantine"></a>
</td>
<td width="33%" valign="top">
  <a href="https://github.com/nisamaasoglu/BOZGUN"><img src="https://raw.githubusercontent.com/nisamaasoglu/BOZGUN/main/docs/demo.gif" width="100%" alt="BOZGUN — colour tracking and lock-on"></a>
</td>
</tr>
<tr>
<td valign="top"><b>Aurora</b><br><sub>Live audio → pitch, timbre, loudness → a volumetric raymarching shader. Every session is a one-time piece.</sub></td>
<td valign="top"><b>LetheFS</b><br><sub>Recall scores decaying along the Ebbinghaus curve into a reversible quarantine. Nothing is deleted silently.</sub></td>
<td valign="top"><b>BOZGUN</b><br><sub>Detect → track → lock on → simulated hit, running with no webcam and no Arduino attached.</sub></td>
</tr>
</table>

---

## Two things I build

<table>
<tr>
<td width="50%" valign="top">

### 🏥 Retrieval-grounded AI

Agents that can only answer from what they actually retrieved, with the guardrail **in front
of** the model rather than behind it.

**[Anamnesis](https://github.com/nisamaasoglu/Anamnesis)** — a hospital information
assistant. Clinical questions are refused before the agent runs. There is no write path at
all: not a disabled one, a missing one, and a test proves it.

<a href="https://github.com/nisamaasoglu/Anamnesis"><img src="https://raw.githubusercontent.com/nisamaasoglu/anamnesis/main/docs/console.png" width="100%" alt="Anamnesis console"></a>

</td>
<td width="50%" valign="top">

### ⚖️ Production web systems

Software that goes to a real client, holds their content, and keeps working after I stop
touching it.

**[Titulus](https://github.com/nisamaasoglu/Titulus)** — live and in daily use. A
2,468-article legislation library, a daily Official Gazette feed, and a database-free admin
panel the lawyer operates himself without calling me.

<a href="https://www.avukatmetinmaasoglu.com"><img src="https://raw.githubusercontent.com/nisamaasoglu/Titulus/main/docs/tools.png" width="100%" alt="Titulus tools panel"></a>

</td>
</tr>
</table>

---

## Everything else

| | What it does | Run it | CI |
|---|---|---|---|
| 🤖 **[Unicorn](https://github.com/nisamaasoglu/Unicorn)**<br><sub>ESP32 · C++</sub> | A solar search-and-rescue rover that raises its own Wi-Fi and serves a command centre from flash. It reports position as a disc with a growing radius, because it has no wheel encoders — and says so. | `./tools/run_tests.sh` | ![](https://github.com/nisamaasoglu/Unicorn/actions/workflows/ci.yml/badge.svg) |
| ❤️ **[Cardia](https://github.com/nisamaasoglu/Cardia)**<br><sub>Arduino · DSP</sub> | A single-lead ECG monitor. R-peaks detected on-device — adaptive threshold, refractory window, interval gating — streamed to a dependency-free dashboard. | `cd web && python3 -m http.server` | — |
| 🧬 **[Helixir](https://github.com/nisamaasoglu/Helixir)**<br><sub>Crypto · PyQt6</sub> | File encryption with a DNA representation layer. AES-256-GCM with scrypt; ciphertext rendered as A/C/G/T and exported to FASTA. The DNA layer is representation, not the cipher. | `python run.py` | ![](https://github.com/nisamaasoglu/Helixir/actions/workflows/ci.yml/badge.svg) |
| 🌸 **[Orchidia](https://github.com/nisamaasoglu/Orchidia)**<br><sub>Vision · Flask</sub> | Orchid identification and care. A classifier reads the species from a photo, then checks environmental readings against that species' ideal range. | `python app.py` | ![](https://github.com/nisamaasoglu/Orchidia/actions/workflows/ci.yml/badge.svg) |

Every command is the whole setup. A reviewer with five minutes should watch the pipeline
run, not fight an install.

---

## What I got wrong

Portfolios only show finished things, which makes everything look equally easy. These are
real defects I found in my own work, and the change each one forced.

<table>
<tr><th align="left" width="16%">Project</th><th align="left" width="42%">What was wrong</th><th align="left" width="42%">What I did about it</th></tr>

<tr><td valign="top"><b>Anamnesis</b></td>
<td valign="top">The offline hashing vectoriser collided. A question about currency hedging retrieved a triage document at score 0.11 — the quiet kind of false positive that makes a RAG demo look fine and be wrong.</td>
<td valign="top">Added a lexical gate: a passage must share a real term with the query before it counts as evidence. Two tests cover it — one asserting off-topic queries return nothing, one asserting that <i>without</i> the gate they would not, so the guard cannot be removed silently.</td></tr>

<tr><td valign="top"><b>Cardia</b></td>
<td valign="top">The dashboard displayed a blood-pressure figure. An AD8232 cannot measure blood pressure.</td>
<td valign="top">Removed it. Panels for values the hardware genuinely cannot produce are gone; the ones that are modelled are labelled as modelled.</td></tr>

<tr><td valign="top"><b>Unicorn</b></td>
<td valign="top">Position was reported as a coordinate. With no wheel encoders, dead reckoning drifts, and a bare coordinate hides that completely. Separately, two motor pins sat on ESP32 strapping pins, and a blocking <code>pulseIn</code> stalled the control loop.</td>
<td valign="top">Position is now a disc with an uncertainty radius, using different constants for calibrated and uncalibrated runs. Pins moved, blocking read replaced — both found by moving the mission logic off the board so it could be tested on a host.</td></tr>

<tr><td valign="top"><b>Helixir</b></td>
<td valign="top">The README framed the DNA layer as part of the encryption. It is not — encoding is not encryption.</td>
<td valign="top">Reframed throughout. AES-256-GCM does the work; the A/C/G/T layer is a representation, and the README says so before it says anything else.</td></tr>

<tr><td valign="top"><b>Orchidia</b></td>
<td valign="top">The interface said "live conditions" over readings that were simulated.</td>
<td valign="top">Says simulated now, in the UI and in the docs.</td></tr>
</table>

The pattern is the same every time. The bug was never the algorithm — it was a claim the
system was not entitled to make.

---

## Check my work in five minutes

```bash
# 1. A grounded answer, and the evidence behind it
git clone https://github.com/nisamaasoglu/Anamnesis && cd Anamnesis
pip install -r requirements.txt && python run.py
#    ask "What are the visiting hours in the intensive care unit?"
#    → the answer names the document and the section it used
#    ask "Do I have cancer?"
#    → refused before any tool runs, with the route to a human

# 2. The tests that hold it together
pip install -r requirements-dev.txt && python -m pytest -q       # 45 passing

# 3. Firmware logic, verified with no hardware attached
git clone https://github.com/nisamaasoglu/Unicorn && cd Unicorn
./tools/run_tests.sh
```

Anamnesis 45 · Helixir 25 · Aurora 16 · Orchidia 13, plus Unicorn's host-compiled C++ suite.
CI runs `ruff` and `pytest` across Python 3.10–3.12 on every push.

---

## How I work

**Test the decision, not the device.** The logic that decides *is this a heartbeat, is this a
survivor, has this file been forgotten, is this passage evidence* is separated from the
hardware or the model feeding it — so it is testable on a laptop with nothing attached.

**State the uncertainty.** An estimate that reports its own error is worth more than a
confident number that quietly lies.

**Say which mode you are in.** Anamnesis reports `generative: false` when no model is
running. Cardia prints `--` when no electrode is attached. Orchidia labels simulated readings
as simulated. A system that hides which mode it is in is lying politely.

**Document what exists.** No roadmaps, no planned features, no claim I could not defend in a
technical interview.

---

<p align="center">
<code>Python</code> · <code>PHP</code> · <code>C++</code> · <code>C#</code> · <code>JavaScript</code> · <code>SQL</code><br>
<code>FastAPI</code> · <code>Flask</code> · <code>Laravel</code> · <code>.NET</code> · <code>React</code> · <code>PyQt6</code><br>
<code>RAG</code> · <code>tool-calling agents</code> · <code>LLM APIs</code> · <code>OpenCV</code> · <code>librosa</code> · <code>scikit-learn</code><br>
<code>Docker</code> · <code>GitHub Actions</code> · <code>SQLite</code> · <code>Arduino / ESP32</code> · <code>Linux</code>
</p>
