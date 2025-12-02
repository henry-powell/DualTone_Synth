# DualTone_Synth — Max/MSP Dual-Engine Tone Synth
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Max/MSP](https://img.shields.io/badge/Environment-Max%2FMSP-blue.svg)](https://cycling74.com/)
![Portfolio Project](https://img.shields.io/badge/Project-Type%3A%20Portfolio-0057b7.svg)
[![Synthesis](https://img.shields.io/badge/Synthesis-Dual%20Engine%20(Additive%20%2B%20Bell)-purple.svg)](#)
![UI](https://img.shields.io/badge/UI-DualTone%20Synth%20Interface-grey.svg)
![Grad Program](https://img.shields.io/badge/Grad_Program-Audio_Technology_(M.A.)-6a1b9a.svg)
![University](https://img.shields.io/badge/American_University-Washington,_DC-002855.svg)

DualTone_Synth is a Max/MSP patch that generates rhythmic dual-tone signals using two selectable synthesis engines and an ADSR-controlled trigger system at 120 BPM. The design focuses on smooth note transitions, no clicks between triggers, and harmonic flexibility.

---

## Features
- **Two synthesis engines**
  - **Additive engine** — sums the first five odd harmonics of a fundamental
  - **Bell-like engine** — blends two partials: *f* and *f × 1.414*
- **ADSR envelope shaping**
  - Attack: 50 ms → 1.0  
  - Decay: 75 ms → 0.7  
  - Sustain: 0.7 held for 125 ms  
  - Release: 200 ms → 0.0
- **K-slider pitch control** — fundamental frequency selected from the UI
- **Click-free playback** — amplitude and envelope ramps avoid discontinuities
- **120 BPM rhythmic trigger** — two notes per second

---

## File Contents
| File | Description |
|------|-------------|
| `DualTone_Synth.maxpat` | Main synthesizer patch |
| `img/screenshot.png` | UI screenshot of the synth |
| `audio/demo.mp3` | Sample audio demo of the patch |

---

## How to Use
1. Open `DualTone_Synth.maxpat` in **Max 8+**
2. Select a frequency using the **K-slider**
3. Pick the synthesis engine (Additive or Bell) using the radio selector
4. Press **Start** to activate the rhythmic 120 BPM trigger
5. Listen and adjust ADSR parameters (if you made them external)

---

## Technical Notes
- Additive synthesis uses partials: *f × {1, 3, 5, 7, 9}*
- Bell synthesis uses partials: *f* and *f × 1.414*
- Envelope is applied at the signal domain to suppress clicks and pops
- Normalized gain staging prevents clipping at the output

---

## Requirements

- Max 8 or later (Cycling '74)
- Audio interface or built-in system audio
- Recommended test settings:
  - 120 BPM trigger (metro = 500 ms)
  - K-slider for pitch selection
  - Output gain below clipping range (-6 dB to -12 dB headroom)
- Works with:
  - Built-in Max DSP settings at 44.1 kHz
  - Optional MIDI input for external pitch control
    
### Optional Enhancements
- MIDI controller for expressive pitch control
- Full-range headphones or monitors for accurate harmonic response

---

© Henry Powell — Audio DSP Development
