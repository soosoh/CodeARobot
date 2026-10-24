# Week 4 — Design Handoff → Constants

## Lecture outline (15–20 min)

**Spectrum anchors:** D3.1 OnShape FRC Robot Organization · D2.1 kit drivetrain · D2.2 Greyt elevator · D2.3 launcher · D2.5 intake · D2.11 swerve

1. CAD-a-thon design rookies produce assemblies (drivetrain, intake, launcher, etc.).
2. Programming team reads the CAD feature list — not the physical robot.
3. Translate CAD → `Constants.java`: motor IDs, CAN IDs, dimensions, gear ratios, PID gains.
4. Design sync protocol — ask questions via GitHub issue (`design-question.md` template).

## Lab checklist

- [ ] Review `DESIGN_HANDOFF.md` feature matrix with design rookies.
- [ ] Fill `Constants.java` placeholders with CAD-a-thon values (mock OK).
- [ ] Create at least one `design-question.md` issue for unclear CAD details.
- [ ] Update subsystems to use `Constants` instead of local numbers.
- [ ] Commit → Push → PR → Merge (`week4-constants`).

## Definition of done

- `Constants.java` has all placeholder fields populated from CAD.
- Every subsystem reads IDs/dimensions from `Constants`.
- At least one design question issue opened or resolved.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Copying constants from another team's robot | Use your own CAD-a-thon values |
| Editing constants in subsystems | Edit only `Constants.java` |
| Waiting for physical measurements | Use CAD values; mark as `// TODO: verify` |
