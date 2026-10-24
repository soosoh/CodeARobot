# Week 6 — Vision & AprilTags

## Lecture outline (15–20 min)

**Spectrum anchors:** C1.6 Intro to FRC Vision Systems · Vision & AprilTags tutorial (ch. 1–7)

1. Why robots need vision — locate game pieces, align to targets.
2. Limelight / PhotonVision — camera processors that publish pose over NetworkTables.
3. AprilTags — fiducial markers with known field positions.
4. Mock camera — since no physical robot, simulate a `VisionProvider` returning pose.
5. NetworkTables — publish/subscribe data between robot and dashboard.

## Lab checklist

- [ ] Create `VisionProvider` interface (`getPose()`, `hasTarget()`).
- [ ] Implement `MockVisionProvider` returning a fixed AprilTag pose.
- [ ] Publish pose to NetworkTables (or a mock table).
- [ ] Create `AlignToTagCommand` using vision pose.
- [ ] Commit → Push → PR → Merge (`week6-vision`).

## Definition of done

- `VisionProvider` interface + mock implementation compile.
- Pose data flows (mock) into a command.
- `AlignToTagCommand` uses vision, not hardcoded values.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Vision command runs without target | Guard with `hasTarget()` |
| Hardcoding tag ID | Read from `Constants.VISION_TAG_ID` |
| Blocking robot loop | Vision reads are non-blocking |
