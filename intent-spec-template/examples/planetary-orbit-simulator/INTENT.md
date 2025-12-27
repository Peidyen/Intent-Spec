# INTENT.md

## Identity
Name: Planetary Orbit Simulator
Version: 1.0
Status: PoC
Owner: Mitch Ronco

## Purpose
This system exists to explore and visualize emergent behavior in
gravitational N-body systems, with particular emphasis on:

- Momentum conservation
- Barycenter motion
- Stability vs chaos in orbital dynamics

Primary question:
“How does momentum transfer and mass distribution affect the motion of
a gravitational system over time?”

## Core Semantics
- Bodies interact via Newtonian gravity
- All bodies exert force on all other bodies
- There is no privileged or fixed reference frame
- Time advances in discrete simulation steps
- Collisions result in inelastic merging by default

## Invariants & Laws
- Total linear momentum of the system must be conserved
- Mass is conserved (merged bodies sum mass)
- Motion emerges solely from forces and initial conditions
- No body is implicitly fixed in space

## User Interaction Model
Users can:
- Add bodies with configurable position, velocity, and mass
- Observe orbital trajectories over time
- Pause, resume, and reset the simulation
- Introduce collisions intentionally
- Observe system drift and center-of-mass motion

## Constraints & Guardrails
- Simulation prioritizes qualitative correctness over numerical precision
- Stable execution is preferred over strict physical accuracy
- Relativistic effects are explicitly excluded
- Units are arbitrary but internally consistent

## Observability & Feedback
The system must make visible:
- Trajectories (paths) of bodies
- Relative motion between bodies
- The system’s center of mass
- Simulation time progression

Observability should make conservation laws discoverable by inspection.

## Non-Goals
- Accurate astronomical prediction
- Real ephemeris or NASA-grade data
- Educational assessment or curriculum
- Long-term numerical stability guarantees

## Exit Criteria
This PoC is considered complete when:
- Users can create stable and unstable orbits
- Inelastic collisions visibly shift the system barycenter
- Momentum conservation is observable without explanation
