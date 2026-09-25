# Atlas — Service Control Board (demo)

Live demo: https://parks-ide-pot-bring.trycloudflare.com/
Backup: https://atlas-oct1-demo.loca.lt/ (if asked for tunnel password, enter your public IP from https://loca.lt/mytunnelpassword)

Fictional clock: Oct 1, 2026 09:00 local. Techs T1, T2, T3.

## Run locally
```
python3 -m http.server 8901 --directory atlas-demo
# open http://localhost:8901/
```

## Permanent deploy (2 min, pick one)
- Vercel: `npx vercel ./atlas-demo --prod` (login once), or drag `atlas-demo/` into vercel.com/new
- Netlify: drag `atlas-demo/` into app.netlify.com/drop
- Cloudflare Pages: `npx wrangler pages deploy atlas-demo --project-name atlas-demo`
No build step. Single static `index.html`.

## 60-sec demo script
1. Open R101 (Urgent, Overdue) → Assign T1 → Set visit Today 10:30
2. Open R104 → Merge into R101 (duplicate gone)
3. Open R107 → Mark Done (customer said fixed, frees T3)
4. Open R102 → Copy status reply → paste to WhatsApp (stops chase calls)
Watch header counts drop live.

## Assumptions (stated in UI, not supplied facts)
SLA: Urgent 4h, High 24h, Normal 72h, Low 7d. Capacity 3/tech. Urgency from keywords.
