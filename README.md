# GFD Web — Preview

This is a ready-to-deploy Next.js preview app for Get Fair Dairy.

## Deploy (no coding)
1. Create a **GitHub** account (if needed) and a new repo named `gfd-web`.
2. Download this ZIP and extract it. Upload all files to the repo via GitHub's web UI (drag & drop).
3. Create a **Vercel** account and click **New Project → Import** your `gfd-web` repo.
4. Add an environment variable `DATABASE_URL` (Neon/Supabase Postgres connection string).
5. In Vercel, enable **Postgres** add-on or paste an external connection string.
6. First deploy will build automatically. Then run migrations & seed locally once, or set up a Vercel script if preferred.

### Local (optional)
```
npm i
cp .env.example .env
# fill DATABASE_URL (Neon/Supabase), then:
npm run prisma:generate
npm run prisma:migrate --name init
npm run db:seed
npm run dev
```