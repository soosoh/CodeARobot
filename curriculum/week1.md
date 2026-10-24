# Week 1 — Repo Setup + Java Essentials

## Lecture outline (15–20 min)

**Spectrum anchors:** C1.1 Intro to Java Programming · C2.0 Install FRC Software Tools

1. What is FRC programming? — robot code runs on the roboRIO, written in Java, using WPILib.
2. The command-based framework — `Robot`, `RobotContainer`, `Subsystem`, `Command`.
3. Java essentials for rookies — classes, interfaces, methods, variables, `public`/`private`, `static final` constants.
4. GitHub Desktop workflow — clone, create branch, commit, push, open PR, merge.

## Lab checklist

- [ ] Clone the template repo with GitHub Desktop (main branch).
- [ ] Create a branch named `week1-setup`.
- [ ] Open `src/main/java/frc/robot/Robot.java` and confirm it compiles.
- [ ] Add your name to `Robot.java` as a comment.
- [ ] Commit → Push → Open a PR → Merge to `main`.

## Definition of done

- Repo cloned locally in GitHub Desktop.
- `./gradlew build` succeeds (or opens in VS Code / WPILib without errors).
- One commit on `main` from your branch.

## Common rookie mistakes + fixes

| Mistake | Fix |
|---------|-----|
| Committing directly to `main` | Always create a branch first: `week1-<yourname>` |
| Forgetting to push after committing | In GitHub Desktop, click "Push origin" after commit |
| Opening PR from wrong branch | Compare `week1-setup` → `main`, not `main` → `main` |
