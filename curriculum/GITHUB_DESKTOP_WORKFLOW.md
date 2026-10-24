# GitHub Desktop Workflow

Rookies use GitHub Desktop (not the command line). No physical robot — code is validated by compiling and running in simulation.

## One-time setup

1. Install GitHub Desktop from desktop.github.com.
2. Sign in to your GitHub account.
3. Clone the team repo:
   - File → Clone Repository → URL tab
   - Paste: `https://github.com/<your-team>/<repo>.git`
   - Choose local folder → Clone

## Weekly cycle (do this every week)

### 1. Start on `main`, pull latest
- Current Branch should be `main`.
- Click **Fetch origin** then **Pull origin** to get latest changes.

### 2. Create a branch for the week
- Current Branch → **New Branch**
- Name: `week1-setup`, `week2-structure`, `week3-interfaces`, … `week8-demo`
- Create Branch

### 3. Write code
- Open the project in VS Code / IntelliJ.
- Complete the week's lab checklist from the curriculum website.

### 4. Commit
- In GitHub Desktop, check the changed files.
- Write a summary (e.g. "Week 3: add Mechanism interface and IntakeSubsystem").
- Add a description (optional but helpful).
- Click **Commit to `weekN-<name>`**.

### 5. Push
- Click the blue **Push origin** button.

### 6. Open a Pull Request
- Click **Create Pull Request** (opens GitHub in your browser).
- Base: `main` ← Compare: `weekN-<name>`
- Fill the PR template.
- Click **Create pull request**.

### 7. Address mentor review
- Mentor comments on the PR.
- Make changes locally, commit, push (PR updates automatically).
- Repeat until approved.

### 8. Merge
- Mentor merges into `main`.
- Delete the branch (optional, keeps things clean).

## Cheat sheet

| Action | Where in GitHub Desktop |
|--------|------------------------|
| Clone repo | File → Clone Repository |
| Switch branch | Current Branch dropdown |
| New branch | Current Branch → New Branch |
| See changes | Changes tab (left panel) |
| Commit | Summary/description → Commit to branch |
| Push | Push origin button (top bar) |
| Pull latest | Pull origin button |
| Open PR | Create Pull Request button |

## Golden rules

- **Never commit directly to `main`.** Always use a feature branch.
- **Pull before you branch.** Start each week from latest `main`.
- **Push after every commit.** So your mentor can review.
- **One branch per week.** Don't mix week 2 and week 3 changes.
