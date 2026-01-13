# TX Driver Operation — Observations

This document records oscilloscope observations of the TX circuit during normal operation.

## General Behavior

When powered, the TX circuit produces a stable, repeating waveform without any external timing source. Operation is self-sustained and persists in the absence of the RX module.

The measured waveforms are non-sinusoidal and exhibit multiple distinct time scales.

## Collector / Primary Coil Node

Measurements at the transistor collector and primary coil (referenced to battery negative) show:

- A repeating sequence consisting of:
  - A sharp voltage spike
  - Followed by damped oscillation (“ringing”) at a frequency on the order of tens of MHz (≈ 50 MHz observed)
- Strongly non-sinusoidal waveform shape
- Repetition rate of spike–ringing events: approximately **3–4 MHz**
- Collector and primary coil waveforms are nearly identical
- Waveform timing and amplitude change slightly with RX proximity and nearby objects

## Transistor Base Node

Measurements at the transistor base (referenced to battery negative) show:

- Approximately sinusoidal waveform at **~3.7–3.8 MHz**
- Positive portion clipped at approximately **+3.5 V**
- Negative portion extending to approximately **−7 V**
- Small high-frequency ringing near the clipped regions

The base is therefore driven by a periodic feedback signal with amplitude limiting and nonlinear behavior.

