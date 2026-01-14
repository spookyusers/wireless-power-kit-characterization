# RX Operation — Observations

This document records oscilloscope and field-probe observations of the RX module during normal operation.

## Measurement Setup

- RX probe reference set to bridge rectifier negative.
- Scope probe set to x10.
- Channel coupling:
  - AC for RX coil measurements
  - DC for rectifier output measurements
- TX operated in strong-coupling orientation unless otherwise noted.

## RX Coil / Rectifier AC Input

Measurements at the RX AC input (coil -> bridge rectifier) show:

- Quasi-sinusoidal waveform present during TX operation.
- Measured period ~156 ns (~6.4 MHz).
- With LED load connected:
  - Observed peak amplitude ~2.2 V.
- With white lampshade LED disconnected:
  - Observed peak amplitude increases to ~4 V.

The RX signal persists without load; connecting the LED significantly damps the received signal amplitude.

## RX Rectifier DC Output

Measurements at the bridge rectifier DC output show:

- With LED load connected:
  - Steady DC output ~3 V.
- With LED load disconnected:
  - DC output increases to ~6 V.

## Pickup Loop Observation at RX

A non-contact pickup loop probe positioned near the RX coil shows:

- Near-sinusoidal waveform detected.
- Measured period ~150 ns (~6.7 MHz).
- Observed peak amplitude ~2 V.
- Moving the TX farther from the RX causes the pickup-loop signal amplitude to decrease smoothly.
- No abrupt frequency change observed; dominant frequency remains ~6-7 MHz.

## Observational Summary

- RX receives a near-sinusoidal signal at ~6-7 MHz.
- RX signal amplitude is strongly affected by electrical loading.
- Rectifier output provides stable DC suitable for LED operation.
- Field strength at RX decreases smoothly with reduced coupling, without sudden frequency shifts.

