# Week 2 — Robot / Subsystem / Command

## Lecture outline (15–20 min)

**Spectrum anchors:** C2.1 Beginner FRC Programming 1 · C2.2 Beginner Subsystems and Commands

1. `Robot.java` — robot lifecycle (`robotInit`, `robotPeriodic`, `teleopInit`, `teleopPeriodic`).
2. `RobotContainer.java` — binds buttons to commands, configures default commands.
3. `Subsystem` — encapsulates one mechanism (drivetrain, intake, shooter). Holds hardware.
4. `Command` — tells a subsystem what to do for a bounded amount of time.
5. Default command — runs when no other command is using the subsystem.

## Lab checklist

- [ ] Create `DrivetrainSubsystem` in `frc.robot.subsystems`.
- [ ] Create `DriveCommand` in `frc.robot.commands`.
- [ ] Wire `DrivetrainSubsystem` + `DriveCommand` in `RobotContainer`.
- [ ] Set a default command on the drivetrain.
- [ ] Commit → Push → PR → Merge (`week2-structure`).

## Definition of done

- Project compiles with no errors.
- `DrivetrainSubsystem` and `DriveCommand` exist in correct packages.
- `RobotContainer` instantiates and links them.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Putting motor logic in `Robot.java` | Move it into the subsystem |
| Forgetting `requires(subsystem)` in command | Add `addRequirements(subsystem)` in constructor |
| No default command | Robot sits still in teleop |
