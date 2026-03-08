# AxialMag – Passive Permanent Magnet Rotary System Concept

**Repository:** [github.com/yourusername/axialmag]  
**Author:** Robert (@BobTheFixer73)  
**Current Status:** Conceptual / Early Prototyping  
**License:** MIT (or choose your preference)

## Overview

AxialMag is an experimental mechanical system that attempts to generate sustained rotary motion using only permanent neodymium magnets, a multi-piston phased cam, and unidirectional force gating — with **no external electrical or mechanical input** after initial assembly imbalance.

The core idea combines:
- 7 axially-reciprocating pistons (each with neodymium magnets)
- A central sinusoidal cam (3 cycles per revolution) converting linear motion to rotation
- Hybrid top/bottom plate magnets with timed attraction-repulsion gating (\~7% pre-hump attract, dead zone at TDC, \~7% post-hump repulse)
- Forced-positive torque contributions (no sign flips, no absolutes — zeros reflect real unloaded states)
- Optional ferrous backing and parasitic shielding for flux concentration

The goal is **not** perpetual motion (which violates conservation laws), but rather a system that exhibits unusually long coasting or graceful decay from magnetic imbalances and dynamic flux interactions, potentially lasting far longer than conventional passive magnetic devices before stopping.

## Key Design Parameters (Small-Scale Prototype Target)

- **Pistons**: 7, equidistant (\~51.4° spacing)
- **Magnets**: N52 neodymium discs, 3 mm thick × 30 mm diameter (15 mm radius)
- **Stroke**: 50 mm total piston travel
- **TDC Gap**: 3 mm minimum between piston and top plate
- **Cam Radius**: \~150 mm (adjustable geometry)
- **Cam Profile**: Sinusoidal, 3 cycles per revolution
- **Power Band**: \~85–90% per 120° piston cycle (dead zone \~10–15% at TDC/N-S junction)
- **Target Volume**: \~4 liters (car-battery-sized enclosure)
- **Adjustability**: Plate altitude (gap) and rotation angle — locked statically for tuning

## Theoretical Performance Estimates (Idealized)

- Peak repulsion per pair at 3 mm gap: \~35 N
- Average force per piston over power band: \~17.5 N
- Total average force (7 pistons): \~122.5 N
- Effective average torque (small scale): \~5 Nm
- Scaled 10× linear: \~5,000 Nm average torque
- Potential mechanical power at 300 RPM: \~157 kW (with generator → \~130–140 kW electrical)

**These are upper-bound idealized figures.** Real performance is expected to be much lower due to force decay with gap, slope-force mismatch, ripple from imperfect phasing, and mechanical losses.

## Physics Discussion – The Core Challenge

The system relies on **conservative magnetic fields** from permanent magnets (position-dependent potential U(r, θ)). Over any full closed cycle (cam rotation → pistons return to starting relative positions), net work done by magnetic forces must be zero:

∫ τ dφ = 0 over one revolution

The attract phase releases stored potential energy into the cam; the repulse phase requires equivalent energy to recharge the field. Phasing, gating, and dynamic flux "unsettling" create directional impulses and may extend coasting time significantly compared to symmetric designs — but do not appear to produce net positive average torque over many cycles without an external energy source.

Losses (bearing friction, air drag, eddy currents, minor hysteresis) ensure eventual stop. The claimed "graceful decay over centuries" would require an extraordinarily low loss rate not supported by known NdFeB magnet behavior (stable over decades, no radioisotope-like depletion).

This is **not** a perpetual motion claim — it is an exploration of how far asymmetric magnetic-mechanical gating can stretch coasting duration before equilibrium is reached.

## Current Challenges

- **Assembly Difficulty**: Strong imbalance torques during piston/plate approach → requires locked shaft, adjustable gaps, and incremental build.
- **Force Decay**: Repulsion drops steeply beyond 3–10 mm gap → narrow effective power windows.
- **Ripple**: Phasing helps but does not eliminate low-torque dead spots.
- **Verification**: No known passive PM-cam system has demonstrated sustained rotation under load; most stop quickly.

## Next Steps / Prototyping Plan

1. **Single-piston test rig** — Validate force vs. gap/angle curves
2. **Adjustable jigs** — Threaded altitude + rotation locking for plates
3. **Incremental assembly** — One piston at a time, large initial gaps
4. **Release & coast-down tests** — Video, RPM logging, decay curve analysis
5. **Add ferrous backing/shielding** — Measure force/torque boost
6. **Small load tests** — If coasting is long, add calibrated friction or tiny generator

Safety first: Use non-magnetic tools, eye protection, gradual gap closure.

## Contributing

This is an open exploration. Pull requests welcome for:
- CAD models / 3D prints
- FEMM / COMSOL magnetostatic simulations
- Better force/slope integration code
- Jig designs for safe assembly

If you build a variant or run tests, please share results (especially coast-down data).

## License

MIT License — feel free to fork, modify, and experiment.

## Disclaimer

This is experimental / conceptual work. No claims of sustained power output are made. Build and test at your own risk — strong magnets can cause injury.

Happy building, and let's see how long it really coasts.

— Robert  
March 2026
