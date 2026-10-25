# Focus Reset Monthly Tracker

A one-file monthly habit tracker. You can tick habits on your phone, edit the list whenever your routine changes, and print any month as a one-page landscape sheet.

## What's inside

| Path | What it is |
| --- | --- |
| `index.html` | The whole app. No build step and no dependencies. |
| `printables/focus-reset-2026-1x-A4.pdf` | Your habits, empty boxes, Oct–Dec 2026 |
| `printables/monthly-habit-tracker-template-A4.pdf` | Blank write-in template (sellable printable) |
| `printables/monthly-habit-tracker-template-Letter.pdf` | Same template, US Letter size |
| `.github/workflows/pages.yml` | Auto-deploys to GitHub Pages on every push to `main` |

## Using it

- **Today card:** tap a habit to tick it for today. Hitting the daily goal (5 by default) wins the day.
- **Grid:** tap any past or current box to fix a missed day. Future days are locked.
- **Edit list:** rename, add, remove and reorder habits and sections. You can also change the title and daily goal. Ticks stay with a habit when you rename it. Every delete can be undone.
- **More → Print:** three options. "This month" prints with your ticks, "clean sheet" prints your habits with empty boxes, and "blank template" prints write-in rows with no dates.
- **More → Back up / Restore:** data lives in your browser's localStorage. To move it to another device, download a backup .json and restore it there.

## Deploy (GitHub Pages, auto on push)

```bash
cd focus-tracker
git init && git add . && git commit -m "Focus tracker"
gh repo create focus-tracker --public --source=. --push
```

Next, on GitHub go to the repo's **Settings → Pages → Source: GitHub Actions**. The workflow then runs on every push.
Your site will be at `https://<your-username>.github.io/focus-tracker/`.

On iPhone, open the URL in Safari and tap **Share → Add to Home Screen**.

## Other free hosts (no workflow file needed)

- **Cloudflare Pages:** Connect the repo. Leave the build command empty and set the output directory to `/`.
- **Netlify:** Connect the repo, or drag the folder onto app.netlify.com/drop.
- **Vercel:** Run `npx vercel` in this folder, or import the repo. Choose the "Other" framework with no build.
