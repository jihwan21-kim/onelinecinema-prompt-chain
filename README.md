# OneLineCinema Prompt Studio (Week 8)

Standalone Next.js prompt-chain management app sharing the existing OneLineCinema Supabase Auth and database.

## Features
- Google OAuth and `profiles.is_superadmin` authorization enforced on UI, database RLS, and generation endpoint.
- Create, rename, delete chains; add, edit, delete and reorder steps.
- Run chained text-generation prompts using OpenAI and persist each intermediate result.
- Browse generated media/history by chain; light, dark and system themes.

## Setup
1. `npm install`
2. Copy `.env.example` to `.env.local` and fill in Supabase publishable key and OpenAI API key.
3. The Week 8 database migration has already been applied to Supabase project `npeoapvqpkpeistlyqto`.
4. Add `http://localhost:3000/auth/callback` and your Vercel domain `/auth/callback` to Supabase Auth redirect allowlist. Enable Google OAuth.
5. `npm run dev`
6. Create a separate GitHub repo and Vercel project; add the same environment variables for production/preview/development.
7. Disable Vercel deployment protection and submit the commit-specific deployment URLs for all three apps.

**Note:** Generated media in this implementation is **text output** from a prompt chain, including captions/descriptions. It does not generate image or video assets. An OpenAI API key is required to run chains.
