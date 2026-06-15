# Camp Pack 🏕️

A mobile-first camping essentials tracker with a Supabase backend.

## Features

- **Home screen** — packing progress overview + category bubbles + recent items
- **Pack List** — items grouped by category, search, filter by packed/unpacked/essential
- **Add Item** — category picker, quantity stepper, essential toggle
- **Progress screen** — overall stats + per-category breakdown
- **Category detail** — drill into any category

## Stack

- Plain HTML/CSS/JS (no build step needed)
- [Supabase](https://supabase.com) for the database

## Deploy to Vercel

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your GitHub repo
4. Leave all settings as default (no build command needed)
5. Click **Deploy** — done!

## Local development

Just open `index.html` in your browser — no server needed.

## Database

The app connects to a Supabase project with two tables:

```sql
-- categories (pre-seeded with 10 camping categories)
id, name, icon, created_at

-- items
id, category_id, name, description, quantity, packed, essential, notes, created_at, updated_at
```

To use your own Supabase project, update these two lines in `index.html`:

```js
const SB  = 'https://YOUR-PROJECT.supabase.co';
const KEY = 'YOUR-ANON-KEY';
```
