# Progress Log

## 2026-01-12
- Cloned repo locally
- Initial inspection of TX/RX modules completed previously.
- No measurements taken yet.
- Next: document TX driver topology and probe oscillation frequency

## 2026-01-12 — Orientation Sensitivity

**Controls**
- TX powered by same 3×AAA battery pack.
- TX–RX separation fixed at ~15 cm.
- No other objects moved during test.
- Indicator: RX red PCB LED and white lampshade LED brightness.

**Observations**
- With TX and RX coil axes parallel:
  - RX LEDs brightest at 0° relative rotation.
  - Brightness decreases with rotation.
  - Near-complete null observed at ~180° rotation.
- With TX and RX coil axes perpendicular:
  - RX LEDs very dim or off at all rotations.
- Rotating TX by 180° with RX fixed reproduces the null, indicating sensitivity depends on relative coil orientation, not absolute orientation in space.

**Notes**
- RX LED brightness varies continuously with relative TX–RX orientation, with a pronounced minimum near 180° rotation.
- The existence of a deep null indicates that coupling depends strongly on relative coil orientation.
- This behavior is inconsistent with isotropic coupling and implies a directional field structure produced by the TX coil.

**Additional Observation**
- Presence of a hand near either TX or RX module noticeably alters RX LED brightness.
- Effect occurs without direct contact.
- Moving the hand closer or farther modulates brightness.
- Effect is reversible and immediate upon hand removal.
- Effect observed even when hand is stationary, suggesting sensitivity to proximity rather than motion.

## 2026-01-13 - Probing Frequency
- Probing TX primary coil relative to battery negative shows a stable, periodic waveform.
- Waveform consists of sharp voltage spikes followed by damped oscillations.
- Repetition frequency of spikes is approximately 3.4 MHz.
- Oscillation persists without RX present.
- Zoomed view of TX waveform shows damped oscillation following each switching spike.
- Ringing period is ~ 20ns.
- Corresponding ringing frequency is ~50MHz.
- Ringing decays within a few cycles before the next switching event.

## 2026-01-12 — TX Driver Circuit (Initial)

- TX uses a single NPN transistor in a self-oscillating configuration.
- Oscillation is sustained by feedback from the coil structure.
- Transistor switches in bursts, injecting energy into the resonant coil.
- Resonant coil rings freely after each switching event.
- Collector waveform matches primary coil waveform, indicating both are part of the same switching node.
- Transistor base shows approximately sinusoidal feedback at ~3.8 MHz.
- Positive portion of base waveform is clipped at ~3.5 V.
- Indicates nonlinear base drive with amplitude limiting.
- Based on scope measurements of collector, coil, and base, TX driver operation is now understood as a self-oscillating, impulsively driven resonant circuit. See TX driver explanation for details.


