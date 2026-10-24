# Week 5 — Commands + Control Loops

## Lecture outline (15–20 min)

**Spectrum anchors:** C2.5 Beginner Control Loops · C2.6 Programming Practices

1. Command groups — run multiple commands in sequence (`SequentialCommandGroup`) or together (`ParallelCommandGroup`).
2. PID controller — `PIDController` from WPILib; P = proportional term only for rookies.
3. Control loop: setpoint → measured value → output → motor.
4. Teleop commands — button-driven, short-lived.
5. Command scheduling — `RobotContainer` configures bindings.

## Lab checklist

- [ ] Create a teleop command that drives forward/backward via button.
- [ ] Add a `PIDController` to hold a position setpoint (mock encoder).
- [ ] Create a `SequentialCommandGroup` auto-ish routine (drive → stop → intake).
- [ ] Bind buttons in `RobotContainer`.
- [ ] Commit → Push → PR → Merge (`week5-commands`).

## Definition of done

- At least one button-bound teleop command works.
- PID loop compiles and updates output based on mock encoder.
- Command group runs in sequence.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Command never ends | Add `isFinished()` returning true |
| PID output not applied to motor | Call `subsystem.set(output)` in `execute()` |
| Multiple commands claim same subsystem | Only one command per subsystem at a time |
