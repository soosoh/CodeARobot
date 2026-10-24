# Design Handoff (CAD-a-thon -> Programming)

**Owner:** Design Liaison (between CAD-a-thon design rookies and programming rookies)  
**Audience:** Programming rookies (Week 4 and beyond)  
**Status:** Draft — to be finalized once CAD-a-thon assemblies are dimensioned  

## Purpose

This document is the contract between the design team (CAD assemblies/sketches) and the programming team (robot code). There is no physical robot; design outputs are CAD assemblies and sketches, not hardware. Programming rookies should treat every value here as a placeholder until the design rookies mark it **CAD-FINAL**.

## Version / Sync Cadence

| Meeting | When | Attendees | Output |
|---|---|---|---|
| CAD Freeze Review | Weekly (design rookies) | Design liaison, programming lead | Updated constants values |
| Design Sync Standup | Twice per week (15 min) | All rookies | Open design questions logged |
| Code Freeze | Week 6 | Both teams | Constants locked for competition code |

## Feature Matrix

| Mechanism (from CAD) | Intended Function | Code Responsibility (subsystem) | Sensor / Actuator Mock Type | CAD Reference |
|---|---|---|---|---|
| Drivetrain (D2.1 kit drivetrain) | Chassis locomotion | `DrivetrainSubsystem` | Motor controller (CAN), Encoder, Gyro/IMU | CAD sketch: base plate + gearbox |
| Greyt elevator (D2.2) | Vertical lift of game piece | `ElevatorSubsystem` | Motor controller (CAN), String potentiometer / limit switch | CAD assembly: elevator |
| Launcher (D2.3) | Shoot game piece at target | `LauncherSubsystem` | Flywheel motor (CAN), Tachometer / encoder, Optical sensor | CAD assembly: launcher |
| Intake (D2.5) | Acquire game piece from floor | `IntakeSubsystem` | Motor controller (CAN or PWM), Beam break / limit switch | CAD assembly: intake |
| Swerve (D2.11) | Holonomic locomotion (alternate drivetrain) | `SwerveSubsystem` | Drive motors (CAN), Steering motors (CAN), Absolute encoders | CAD assembly: swerve module |

> Only one drivetrain (D2.1 OR D2.11) will be programmed. The choice is a design decision — see Design Sync below.

### Subsystem -> Command Mapping (placeholder)

| Subsystem | Default Command | Teleop Command |
|---|---|---|
| Drivetrain | `DefaultDriveCommand` | `TeleopDriveCommand` |
| Elevator | `HoldPositionCommand` | `ElevatorSetpointCommand` |
| Launcher | `HoldSpeedCommand` | `LauncherFireCommand` |
| Intake | `IntakeIdleCommand` | `IntakeInCommand` / `IntakeOutCommand` |
| Swerve | `DefaultSwerveCommand` | `TeleopSwerveCommand` |

## CAD-a-thon -> Spectrum Mechanism Video Mapping

| CAD-a-thon Mechanism | Spectrum Exploration Video | What Programming Rookies Should Watch For |
|---|---|---|
| Drivetrain (kit) | D2.1 kit drivetrain | Motor count per side, gearbox reduction, wheel diameter, encoder placement |
| Elevator | D2.2 Greyt elevator | Stage count, cascade vs continuous, string/chain drive, limit switch locations |
| Launcher | D2.3 launcher | Flywheel RPM target, hood angle adjustment, feeder timing, sensor placement |
| Intake | D2.5 intake | Roller speed, deployment mechanism, beam-break / limit switch locations |
| Swerve (alternate) | D2.11 swerve | Module count, drive/steer motor pairing, absolute encoder offset, module geometry |

Videos are referenced by Spectrum exploration ID; ask the design liaison for links if not bookmarked.

## Design Sync Protocol

Programming rookies request design clarification via a GitHub issue using the template at `.github/ISSUE_TEMPLATE/design-question.md`.

### How to request clarification

1. **Check first:** Search open/closed issues for an existing design question about the same mechanism. Do not duplicate.
2. **Create issue:** Use the "Design Question" template. Title format: `[DESIGN] <Mechanism> - <short question>`.
3. **Tag:** Add labels `design-question` and the mechanism area (e.g. `drivetrain`, `elevator`).
4. **Assign:** Assign the design liaison.
5. **Wait:** Do not guess values. Block on the answer before committing code that depends on the unknown constant.
6. **Close:** When answered, update `constants_template.java` with the real value and close the issue.

### Example design questions

- "What is the wheel diameter (inches) for the D2.1 drivetrain?"
- "Does the D2.2 elevator use a string potentiometer or a limit switch for bottom detection?"
- "Which CAN IDs are reserved for the D2.11 swerve drive vs steer motors?"
- "Is the D2.3 launcher flywheel single or dual wheel?"

## Using constants_template.java

1. Copy `constants_template.java` into `src/main/java/frc/robot/constants/Constants.java`.
2. Fill every `// TODO: fill from CAD-a-thon` placeholder with the value from the CAD-a-thon design rookies (via Design Sync).
3. Do not hard-code magic numbers elsewhere in robot code; reference `Constants.*` instead.
4. Keep units consistent: dimensions in inches, angles in degrees, time in seconds, speeds in native motor units unless noted.

## Definition of Done for Handoff

- [ ] Every mechanism in the Feature Matrix has a code owner (subsystem).
- [ ] `constants_template.java` has no remaining `// TODO` placeholders.
- [ ] All open `design-question` issues are resolved or have an agreed workaround.
- [ ] Drivetrain choice (D2.1 vs D2.11) is documented and code reflects the choice.
- [ ] Programming rookies can build the robot project without asking design for any dimension/ID.
