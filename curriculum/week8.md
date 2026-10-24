# Week 8 — Telemetry + Mock Match

## Lecture outline (15–20 min)

**Spectrum anchors:** Telemetry, Logs and Replay · Control Systems (ch. 1–5)

1. NetworkTables — publish values to SmartDashboard / ShuffleBoard.
2. What goes on driver's screen — motor speeds, setpoints, vision pose, auto state.
3. Logs — robot writes data; replay after match.
4. Control systems recap — CAN bus, motor controllers, power.
5. Mock match demo — run teleop + auto end-to-end in simulation.

## Lab checklist

- [ ] Publish 3+ values to SmartDashboard (speed, setpoint, vision pose).
- [ ] Add a dashboard button to trigger a command.
- [ ] Create a log entry on state change (auto → teleop).
- [ ] Run full mock match: auto → teleop → end.
- [ ] Final commit → Push → PR → Merge (`week8-demo`).

## Definition of done

- Dashboard displays live robot values.
- Mock match runs auto then teleop without crashes.
- All 8 weeks merged to `main`.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Dashboard not updating | Publish in `robotPeriodic()`, not once |
| Logging too much | Log only state changes |
| Demo crashes | Test each week incrementally |
