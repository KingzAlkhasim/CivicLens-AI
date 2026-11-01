# AI4Elections: Multilingual Voter-Information & Claim-Check Assistant

Entry for the #AI4Elections Hackathon (Rise Networks / INEC). Hausa-first, multilingual assistant that
answers voter questions ONLY from official public sources, cites them, and sends uncertain claims
to human review.

## Safety rules (hackathon requirements, apply to every contributor)
- Non-partisan: no party/candidate content, no persuasion.
- Public, synthetic or authorised data only. NEVER commit voter registers or personal data.
- The app never declares results or fraud. Uncertain = "check with INEC" + human review.
- Mock data in /mock is SAMPLE text, not real INEC information.

## Structure
- `docs/API_CONTRACT.md`  endpoints and response shapes (frontend builds against this)
- `mock/`                 sample JSON responses for every endpoint
- `tasks/`                one file per task, with acceptance criteria
- `frontend/`             React + TypeScript + Tailwind app
- `backend/`              API, retrieval, claim-check (maintainers only for now)

## Frontend setup (maintainer runs this once, then commits)
```
cd frontend
npm create vite@latest . -- --template react-ts
npm install
npm install -D tailwindcss @tailwindcss/vite
npm run dev
```

## Workflow
See CONTRIBUTING.md. Short version: branch, small PR, maintainer reviews, squash merge.
