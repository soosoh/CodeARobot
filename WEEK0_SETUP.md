# Week 0 Setup — CodeARobot (Virtual Robot)

This guide walks rookies through cloning the repo, creating a weekly branch, and committing in **GitHub Desktop**. No physical robot is needed — we code a virtual robot that matches the CAD design.

## Prerequisites
- Install [GitHub Desktop](https://desktop.github.com/)
- Install [JDK 17](https://adoptium.net/) (WPILib requires Java 17)
- Install [VS Code](https://code.visualstudio.com/) with the **WPILib** extension (optional but recommended)

## 1. Clone the repository

Open GitHub Desktop → **File → Clone repository**.

Clone URL:
```
https://github.com/hammerhead226/CodeARobot.git
```

- **Local path:** `C:\Users\Robotics\Documents\CodeARobot`
- Click **Clone**.

## 2. Create a branch for the week

Always work on a feature branch, never directly on `main`.

In GitHub Desktop:
1. Click the **Current branch** dropdown (shows `main`).
2. Choose **New branch**.
3. Name it `week1-setup` (use `week2-setup`, `week3-setup`, etc. for later weeks).
4. Branch from: `main`
5. Click **Create branch**.

## 3. Make changes

- Open `C:\Users\Robotics\Documents\CodeARobot` in VS Code.
- Edit code under `src/main/java/frc/robot/`.
- Subsystems → `src/main/java/frc/robot/subsystems/`
- Commands → `src/main/java/frc/robot/commands/`
- Constants → `src/main/java/frc/robot/constants/Constants.java`

## 4. Commit and push

In GitHub Desktop:
1. You'll see your changed files in the left panel under **Changes**.
2. Check the boxes for files to include.
3. Enter a **Summary** (required), e.g. `week1: add drivetrain subsystem`.
4. Add an optional **Description**.
5. Click **Commit to week1-setup**.
6. Click **Publish origin** (first time only) to push to GitHub.
7. After that, click **Push origin** to push new commits.

## 5. Open a pull request (PR)

1. Go to the repo on GitHub.com.
2. Click **Compare & pull request** for your `week1-setup` branch.
3. Title: `week1: <what you did>`
4. Request a review from a mentor.
5. After approval, **Merge pull request** into `main`.
6. Delete the branch (optional).

## Branch naming
- `week1-setup`, `week2-setup`, ..., `week8-setup`
- Always branch from `main`, merge back to `main` via PR.

## Helpful GitHub Desktop commands (what the buttons do)

| Action | GitHub Desktop button | Equivalent git command |
|--------|----------------------|------------------------|
| Clone | Clone repository | `git clone <URL>` |
| New branch | New branch | `git checkout -b week1-setup` |
| Commit | Commit to <branch> | `git add -A && git commit -m "msg"` |
| Push | Push origin | `git push origin week1-setup` |
| Pull | Pull origin | `git pull origin main` |
