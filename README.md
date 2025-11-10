# My Free Blog (Next.js + Supabase) - Starter

This is a minimal, free-friendly blog starter using Next.js + Tailwind and Supabase (client).
It includes a simple mobile-friendly `/admin` page for creating/editing posts (Markdown), 
and a basic frontend listing + post detail page.

## Quick start (local)

1. Install dependencies:
```bash
npm install
```

2. Create `.env.local` (see `.env.example`) and fill:
```
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key
NEXT_PUBLIC_SITE_NAME=My Blog
ADMIN_PASSWORD=your_admin_password
```

3. Run dev server:
```bash
npm run dev
```

Open http://localhost:3000 and http://localhost:3000/admin

## Supabase setup

In Supabase SQL editor run `sql/supabase_schema.sql` to create the `posts` table.

## Deploy

1. Push to GitHub
2. Import project into [Vercel](https://vercel.com)
3. Add the environment variables in Vercel dashboard (same as .env.local). 
   Do NOT put service role keys into client env variables.

## Notes

- This starter uses client-side Supabase for simplicity. For production, protect write operations
  via server-side APIs or use Supabase Row Level Security and authenticated users.
- The admin password in this starter is a simple check; for stronger security use Supabase Auth or NextAuth.
