# Atlas — Service Control Board (demo)

Live demo: https://pika919.github.io/atlas-demo/
Demo video (40s): https://github.com/PiKa919/atlas-demo/blob/main/demo.mp4

Fictional clock: Oct 1, 2026 09:00 local. Techs T1, T2, T3. All data synthetic.

## Setup

No dependencies, no build step, no environment variables, no backend.
It is one static `index.html` (Tailwind + Chart.js via CDN). State lives in
browser localStorage only.

Run locally with any static server, e.g.:

```
python3 -m http.server 8901
# open http://localhost:8901/
```

Or deploy by uploading `index.html` to any static host
(GitHub Pages, Netlify Drop, Vercel, Cloudflare Pages).

## 60-sec demo script

1. Tour auto-opens on first visit (or click Take tour).
2. Open R101 (Urgent, Overdue) → Assign T1 → Visit time Today 10:30.
3. Open R104 → Merge into R101 (duplicate gone, awkward case 1).
4. Open R105 → vague report with missing equipment ID (awkward case 2).
5. Open R107 → Mark Done (customer confirmed fixed, frees T3).
6. Open R102 → Copy status reply → paste to WhatsApp (stops chase calls).
7. Filter by urgency, click a map pin to jump to its ticket.

Watch header counts and charts move live.

## Assumptions (stated in UI, not supplied facts)

SLA: Urgent 4h, High 24h, Normal 72h, Low 7d. Capacity 3 active jobs per
tech. Urgency keyword-scored. No real email/WhatsApp integration — intake is
simulated via the Log request form.
