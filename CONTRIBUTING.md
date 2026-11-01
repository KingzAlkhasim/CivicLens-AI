# Contributing

1. Pick ONE task from `tasks/` (the maintainer assigns it).
2. Pull latest main: `git checkout main && git pull`
3. Create a branch: `git checkout -b feat/task-01-chat-screen`
4. Build only what the task asks. Use data from `/mock` via a local import, not a live server.
5. Run `npm run build` and `npm run lint` before pushing.
6. Push and open a Pull Request into `main`. Fill in the PR template, add a screenshot (mobile width).
7. The maintainer reviews. Fix comments on the same branch, then it is squash-merged.

Rules: never push to main, one task per PR, no personal data, ask early if stuck (stuck > 1 hour = message).

## Maintainer: GitHub settings
- Settings > Branches: protect `main`; require a pull request and 1 approval; block force pushes.
- Settings > Collaborators: add teammates.
