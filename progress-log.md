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
  - RX LEDs brightest at 0deg relative rotation.
  - Brightness decreases with rotation.
  - Near-complete null observed at ~180deg rotation.
- With TX and RX coil axes perpendicular:
  - RX LEDs very dim or off at all rotations.
- Rotating TX by 180deg with RX fixed reproduces the null, indicating sensitivity depends on relative coil orientation, not absolute orientation in space.

**Notes**
- RX LED brightness varies continuously with relative TX–RX orientation, with a pronounced minimum near 180deg rotation.
- The existence of a deep null indicates that coupling depends strongly on relative coil orientation.
- This behavior implies a directional field structure produced by the TX coil.

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

## 2026-01-13 — TX Driver Circuit (Initial)

- TX uses a single NPN transistor in a self-oscillating configuration.
- Oscillation is sustained by feedback from the coil structure.
- Transistor switches in bursts, injecting energy into the resonant coil.
- Resonant coil rings freely after each switching event.
- Collector waveform matches primary coil waveform, indicating both are part of the same switching node.
- Transistor base shows approximately sinusoidal feedback at ~3.8 MHz.
- Positive portion of base waveform is clipped at ~3.5 V.
- Indicates nonlinear base drive with amplitude limiting.
- Based on scope measurements of collector, coil, and base, TX driver behavior is consistent with a self-oscillating, impulsively driven resonant circuit. See TX driver explanation for details.

## 2026-01-14 - RX Module Analysis

### Rectifier probe

- RX probe reference set to rectifier negative.
- Probed RX AC input (coil -> bridge rectifier).
- Observed quasi-sinusoidal waveform at RX.
- Measured period ~ 156 ns (~ 6.4 MHz).
- Measured AC amplitude ~ 2.2 V with LED load connected.
- Disconnecting the white lampshade LED increased RX AC amplitude to ~ 4 V.
- RX signal persists without load; LED load significantly damps the received signal.
- Rectifier DC output ~ 3 V with LED load; rises to ~ 6 V with load disconnected.

### Pickup loop probe at RX

- Pickup loop positioned near the RX coil.
- Observed a near-sinusoidal waveform at the pickup loop.
- Measured period ~ 150 ns (~ 6.7 MHz).
- Observed amplitude ~ 2 V (peak) with strong TX–RX coupling.
- Moving the TX farther from the RX causes the pickup-loop signal amplitude to decrease smoothly.
- No abrupt frequency change observed; dominant frequency remains ~ 6–7 MHz.










































