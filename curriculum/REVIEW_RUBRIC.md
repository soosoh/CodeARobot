# Review Rubric

Mentors use this to review rookie pull requests. No physical robot — validation is by compilation and logic.

## Weekly review criteria

| Criterion | Pass | Notes |
|-----------|------|-------|
| Project compiles (`./gradlew build`) | ☐ | No errors |
| Classes in correct packages (`frc.robot.subsystems.*`, `frc.robot.commands.*`) | ☐ | |
| Interfaces used where appropriate | ☐ | Week 3+ |
| Constants in `frc.robot.constants` (no magic numbers) | ☐ | Week 4+ |
| Command/subsystem separation | ☐ | No motor logic in `Robot.java` |
| `requires()` / `addRequirements()` in commands | ☐ | |
| Default command set on subsystems | ☐ | Week 2+ |
| Week-specific lab checklist complete | ☐ | See weekN.md |

## GitHub Desktop workflow (rookies)

1. **Clone** the repo (File → Clone Repository → paste URL).
2. **Create branch** — Current Branch → New Branch → `weekN-<yourname>`.
3. **Edit code** in VS Code / IntelliJ.
4. **Commit** — write summary + description → Commit to `<branch>`.
5. **Push origin** — blue button in top bar.
6. **Open PR** — click "Create Pull Request" on GitHub (or via GitHub Desktop).
7. **Address review** — make changes, commit, push (PR updates automatically).
8. **Merge** — after approval, merge into `main`, delete branch.

## Red flags that block merge

- Uncommitted changes left in working tree
- Broken build / compilation errors
- Hardcoded magic numbers (motor IDs, dimensions, gains)
- Motor/controller logic inside `Robot.java`
- Missing `addRequirements()` in a command
- PR from `main` instead of a feature branch

## PR template

See `.github/PULL_REQUEST_TEMPLATE.md`. Rookies must fill out: week number, lab checklist completed, how tested, design-handoff reference.
