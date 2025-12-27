# RAG.md

## Domain Context
This system is based on classical orbital mechanics and Newtonian gravity.
It intentionally simplifies reality to highlight first-order dynamics and
emergent behavior rather than precision astronomy.

The simulator is designed as a thinking tool, not a calculator.

## Canonical Definitions
- Body: A point mass with position, velocity, and mass
- Barycenter: The center of mass of all bodies in the system
- Inelastic collision: A collision in which bodies merge and conserve
  total momentum but not kinetic energy
- Reference frame: The coordinate system in which motion is observed;
  no frame is privileged

## Reference Models
Newton’s law of universal gravitation:

F = G * (m₁ * m₂) / r²

Acceleration:
a = F / m

Momentum:
p = m * v

Total system momentum:
Σ pᵢ = constant

Center of mass:
R = (Σ mᵢ * rᵢ) / (Σ mᵢ)

## Examples & Scenarios
- Circular orbit: A body initialized with tangential velocity
- Eccentric orbit: Velocity slightly above or below circular
- Collision test: A fast body impacts a massive central body,
  causing the merged mass to drift
- Binary system: Two similar-mass bodies orbit a shared barycenter

## Known Approximations
- Discrete time integration (Euler or Verlet)
- Artificial collision radius
- Scaled gravitational constant
- No energy correction or damping beyond collisions

## Failure Modes
- Large time steps can cause numerical instability
- Close encounters may eject bodies unrealistically
- High mass ratios may exaggerate drift visually

These are acceptable within PoC scope.

## External References
- Classical Mechanics — Goldstein
- Orbital Mechanics — Prussing & Conway
- n-body problem (general reference)
