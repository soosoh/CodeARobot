# Week 7 — Autonomous Paths

## Lecture outline (15–20 min)

**Spectrum anchors:** Paths & Autonomous tutorial (ch. 1–8)

1. What an auto is — 15-second pre-programmed routine at match start.
2. Paths — sequence of waypoints the robot follows.
3. Path following — drive along path while correcting with PID/odometry.
4. Red/Blue alliance — mirror paths for opposite side.
5. Events during auto — intake, shoot, stop at waypoints.

## Lab checklist

- [ ] Define 3–5 waypoints for a mock auto path.
- [ ] Create `FollowPathCommand` that drives through waypoints.
- [ ] Add alliance switch (red vs blue mirrored path).
- [ ] Add one auto event (e.g. intake on at waypoint 2).
- [ ] Commit → Push → PR → Merge (`week7-autonomous`).

## Definition of done

- Auto path compiles and follows waypoints (mock odometry).
- Red/Blue toggle changes path direction.
- At least one auto event triggers mid-path.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Auto runs in teleop | Guard with `DriverStation.isAutonomous()` |
| Path not mirrored | Negate X coordinates for blue alliance |
| No waypoint tolerance | Stop when within `Constants.AUTO_WAYPOINT_TOLERANCE` |
