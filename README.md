<h1 align="center">Nisa Maaşoğlu</h1>
<h3 align="center">Software Engineer &middot; Real-Time Systems &middot; Applied AI</h3>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=21&pause=1200&color=6C63FF&center=true&vCenter=true&width=620&lines=Turning+live+signals+into+decisions;Audio%2C+biosignals%2C+video%2C+sensors;Every+project+runs+on+a+clean+clone;What+can't+be+measured+is+labelled%2C+not+faked;I+only+ship+what+I+can+defend" alt="" />
</p>

<p align="center">
  <a href="https://linkedin.com/in/nisamaasoglu"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:nisamaasoglu7@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://img.shields.io/badge/open%20to-software%20engineering%20roles-2ea043?style=flat-square" alt="Open to work" />
</p>

---

I build systems where a **live signal has to become a decision**: a microphone, an
electrode, a camera frame, an accelerometer. The interesting part is never the sensor —
it is what you are allowed to conclude from it, and how you behave when the answer is
*I don't know yet*.

That question shows up everywhere in my work. An ECG monitor that prints `--` instead of
a number when no electrode is attached. A rover that reports its position as a disc with
a growing radius, because it has no wheel encoders and says so. A dashboard that draws
simulated data in a different colour from measured data, so nobody can confuse the two.

**Two rules I hold to across every repository here:**

- **A clean clone runs.** No hardware, no trained model, no API key, no dataset.
- **What cannot be measured is labelled, not faked.** Simulated values are marked as
  simulated, in the UI and in the code.

---

## Projects

| | What it does | Run it |
|---|---|---|
| 🎵 **[Aurora](https://github.com/nisamaasoglu/Aurora)**<br><sub>Signals · Graphics</sub> | Real-time generative art. Live audio pitch, timbre and loudness drive a volumetric raymarching GLSL shader — every session is a one-time, non-repeatable artwork. | `python main.py`<br><sub>no mic → simulation</sub> |
| 🧠 **[LetheFS](https://github.com/nisamaasoglu/LetheFS)**<br><sub>Systems · Cognition</sub> | An autonomous forgetting file system. Recall scores decay along the Ebbinghaus curve into a reversible quarantine you resolve from a live dashboard. Nothing is ever deleted silently. | `python run.py`<br><sub>sandboxed by default</sub> |
| ❤️ **[Cardia](https://github.com/nisamaasoglu/Cardia)**<br><sub>IoT · Signal Processing</sub> | Single-lead ECG monitor. An AD8232 and an Arduino detect R-peaks on-device — adaptive threshold, refractory window, interval gating — and stream heart rate to a dependency-free dashboard. | `cd web && python3 -m http.server`<br><sub>falls back to a synthetic ECG</sub> |
| 🎯 **[BOZGUN](https://github.com/nisamaasoglu/BOZGUN)**<br><sub>Computer Vision · Robotics</sub> | Colour-tracking turret. OpenCV maps a target's pixel position to pan/tilt servo angles over serial and marks it with a laser. Simulated hit, no projectile. | `python bozgun.py --demo`<br><sub>no webcam, no Arduino</sub> |
| 🌸 **[Orchidia](https://github.com/nisamaasoglu/Orchidia)**<br><sub>AI · Web</sub> | Orchid identification and care assistant. A classifier reads the species from a photo, then checks environmental readings against that species' ideal ranges. | `python app.py`<br><sub>demo backend, no model needed</sub> |
| 🧬 **[Helixir](https://github.com/nisamaasoglu/Helixir)**<br><sub>Cryptography · Desktop</sub> | File encryption with a DNA representation layer. AES-256-GCM with scrypt; the ciphertext is rendered as an A/C/G/T sequence and exported to FASTA. The DNA layer is representation, not the cipher. | `python run.py`<br><sub>PyQt6 desktop app</sub> |

Every command above is the whole setup. That is deliberate: a reviewer with five minutes
should see the pipeline run, not fight an install.

---

## How I work

- **Test the decision, not the device.** The logic that decides *is this a heartbeat, is
  this a survivor, has this file been forgotten* is separated from the hardware that
  feeds it — so it is testable on a laptop with no board attached.
- **Document what exists.** No roadmap sections, no planned features, no claims I could
  not defend in a technical interview.
- **State the uncertainty.** An estimate that reports its own error is worth more than a
  confident number that quietly lies.

---

## Tech

**Languages** &nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![GLSL](https://img.shields.io/badge/GLSL-5586A4?style=flat-square&logo=opengl&logoColor=white)

**Frameworks & libraries** &nbsp;
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Qt](https://img.shields.io/badge/PyQt6-41CD52?style=flat-square&logo=qt&logoColor=white)

**Embedded & tools** &nbsp;
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![PlatformIO](https://img.shields.io/badge/PlatformIO-FF7F00?style=flat-square&logo=platformio&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

---

<p align="center">
  <sub>Aksaray University, Software Engineering · Source code available on request for private work</sub>
</p>
