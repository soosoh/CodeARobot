# Week 3 — Subsystems + Java Interfaces

## Lecture outline (15–20 min)

**Spectrum anchors:** C2.3 Beginner Motors for FRC · C2.4 Encoders & Spark Max Controls

1. Java `interface` — defines *what* a subsystem can do, not *how*.
2. Example: `Mechanism` interface with `set(double)`, `stop()`, `getPosition()`.
3. Motors and motor controllers (Spark Max, Talon FX) — simulated since no physical robot.
4. Encoders — report position/distance; used for feedback.
5. Constants — hardware IDs live in `frc.robot.constants`, never hardcoded.

## Lab checklist

- [ ] Create `Mechanism.java` interface in `frc.robot.subsystems`.
- [ ] Implement `Mechanism` in a mock subsystem (e.g. `IntakeSubsystem`).
- [ ] Add mock motor + encoder fields with IDs from `RobotMap`.
- [ ] Add `set(double speed)` and `getPosition()` implementations.
- [ ] Commit → Push → PR → Merge (`week3-interfaces`).

## Definition of done

- Interface `Mechanism` compiled and implemented.
- Mock subsystem uses `RobotMap` constants for IDs.
- No magic numbers in subsystem code.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Hardcoding `new SparkMax(5)` | Use `RobotMap.INTAKE_MOTOR_ID` |
| Interface missing methods | Add all methods subsystem needs |
| Subsystem knows about another subsystem | Subsystems are independent; coordinate via commands |
