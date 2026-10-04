# WAINEMAN Dashboard (web-app)

Statische web-app (één `index.html`) op Vercel. Data en login via Supabase:

- Edge function `crm` (project `joucxqkpyhpxazdhhiic`): inloggen met de toegangscode, data lezen/schrijven, websitestatistiek, AI.
- Tabel `kv`: alle dashboard-documenten (`crm/meta`, `crm/added`, `crm/rest`, …). RLS aan, alleen bereikbaar via de edge function.
- Geplande taken (lead factory, uurlijkse sync) schrijven direct in `kv`.

AI-functies (mail persoonlijk maken, dagplan) gaan aan zodra `ANTHROPIC_API_KEY` als secret in Supabase → Edge Functions staat.

Installeren als app: open de site in Safari → Deel → "Zet op beginscherm".
