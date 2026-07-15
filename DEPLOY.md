Deployment steps (Vercel)
-------------------------

1. Confirm `vercel.json` exists (already added).
2. DO NOT commit real secrets. Use the Vercel dashboard to set the following environment variables:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_PUBLISHABLE_KEY`
   - `VITE_SUPABASE_PROJECT_ID`
   - `SUPABASE_SERVICE_ROLE_KEY` (only if server-side functions need it)
   - `OPENAI_API_KEY` (if used)

3. Configure the Vercel project to use the GitHub repository and the `main` branch.
   - Build command: `npm run build`
   - Output directory: `dist`

4. Deploy. After deployment, verify the site and rotate keys if any were exposed.

Notes:
- If you accidentally committed secrets, rotate keys immediately and consider removing them from history.
- If you want GitHub Actions to deploy instead of Vercel Git integration, provide a `VERCEL_TOKEN` and I can add an Action.
