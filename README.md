# KingDocs

Small app built with TanStack Start + Vite. This repo contains the frontend, server entry, and deployment configs for Vercel.

Quick Start (local)
- Install: `npm install`
- Dev server: `npm run dev`
- Build: `npm run build`
- Preview build: `npm run preview`

Environment
- Copy `.env.example` to `.env` and fill values for local development. Key variables used by the app:
  - `VITE_SUPABASE_URL`
  - `VITE_SUPABASE_PUBLISHABLE_KEY`
  - `VITE_SUPABASE_PROJECT_ID`
  - `SUPABASE_SERVICE_ROLE_KEY` (server only)
  - `OPENAI_API_KEY` (if used)

Deployment (Vercel)
- This repo includes `vercel.json` and a GitHub Actions workflow that can deploy to Vercel on pushes to `main`.
- Two recommended deployment methods:
  1. Connect the GitHub repo in the Vercel dashboard (recommended). Vercel will auto-deploy on merges to `main`.
  2. Use the included GitHub Action: set these repository secrets in GitHub Settings → Secrets:
     - `VERCEL_TOKEN`, `VERCEL_ORG_ID`, `VERCEL_PROJECT_ID`
     After adding secrets, you can run the workflow manually from Actions or push to `main`.

Notes
- Do NOT commit real secrets. Use `.env.example` as a template and store real values in GitHub Secrets or Vercel settings.
- If secrets were committed earlier, rotate them immediately.

More
- See [DEPLOY.md](DEPLOY.md) for additional deployment notes and environment guidance.
