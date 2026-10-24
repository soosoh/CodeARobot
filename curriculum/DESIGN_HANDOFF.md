# Design Handoff

CAD-a-thon design rookies produce the robot design. Programming rookies translate it into code. There is no physical robot — design outputs are CAD assemblies and sketches.

## Feature Matrix

| Mechanism | CAD Source | Function | Code Responsibility | Mock Sensor/Actuator |
|-----------|------------|----------|---------------------|----------------------|
| Drivetrain | D2.1 kit drivetrain | Move around field | `DrivetrainSubsystem` | 2 Spark Max + encoders |
| Intake | D2.5 intake | Pick up game piece | `IntakeSubsystem` | 1 Spark Max + beam break |
| Launcher | D2.3 launcher | Shoot game piece | `LauncherSubsystem` | 2 Spark Max + encoder |
| Elevator | D2.2 Greyt elevator | Lift game piece | `ElevatorSubsystem` | 1 Spark Max + encoder |
| Swerve module | D2.11 swerve | Steer + drive wheels | `SwerveSubsystem` | 4 Spark Max + encoders + gyro |

## Constants.java Template

```java
package frc.robot.constants;

public final class Constants {
  // TODO: fill from CAD-a-thon design

  // Drivetrain
  public static final int LEFT_MOTOR_ID = 0;      // TODO
  public static final int RIGHT_MOTOR_ID = 1;     // TODO
  public static final double DRIVETRAIN_TRACKWIDTH_INCHES = 24.0; // TODO

  // Intake
  public static final int INTAKE_MOTOR_ID = 2;    // TODO
  public static final int INTAKE_BEAM_BREAK_ID = 0; // TODO

  // Launcher
  public static final int LAUNCHER_MOTOR_ID = 3;  // TODO
  public static final double LAUNCHER_SETPOINT_RPM = 4000.0; // TODO

  // Elevator
  public static final int ELEVATOR_MOTOR_ID = 4;  // TODO

  // Vision
  public static final int VISION_TAG_ID = 1;      // TODO

  // Autonomous
  public static final double AUTO_WAYPOINT_TOLERANCE_INCHES = 2.0; // TODO

  private Constants() {}
}
```

## Design Sync Protocol

1. Programming rookie opens a GitHub issue using `.github/ISSUE_TEMPLATE/design-question.md`.
2. Tag `@design-rookie` and link the relevant CAD assembly.
3. Design rookie replies in the issue with the value or a CAD screenshot.
4. Programming rookie updates `Constants.java` and references the issue number in the commit.

## CAD → Spectrum Mechanism Video Map

| CAD Mechanism | Spectrum Video |
|---------------|----------------|
| Drivetrain | D2.1 Exploration of the FRC Kit Drivetrain |
| Elevator | D2.2 Exploration of the WCP Greyt Elevator |
| Launcher | D2.3 Exploring the 2017 Spectrum Launcher |
| Intake | D2.5 Exploration of the 2020 Spectrum Intake |
| Swerve | D2.11 Beginner Swerve |
