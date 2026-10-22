# Muse × HighLevel — Agency ROI Calculator

The interactive calculator from slide 13 of the **HighLevel Dallas Chapter** deck
*"The Agent Layer: Muse × HighLevel"* (Nathan Brown, Hivergent AI), packaged as a
standalone web app so anyone can run their own numbers — or remix it.

**Example math — your numbers, your call.** Every output is computed live from the
inputs below. Nothing here is a guarantee or a benchmark; plug in your real figures.

## What it does

Inputs:
- Hours per week you (or your team) burn on follow-up, admin & content **per account**
- Your time value ($/hour)
- The % of that busywork Muse realistically takes off the plate
- How many client accounts you run this across
- Your stack cost per account: HighLevel plan (Starter $97 / Unlimited $297 / Agency Pro $497) + Muse (free tier $0; paid plans from ~$20/mo, reported)
- What a part-time ops hire would cost you per month (comparison)

Outputs:
- Hours back per month · Dollar value of that time · Net after stack cost
- Annual net · Stack payback time · Savings vs the part-time hire

## Run it

No build step. Open `index.html` in any browser, or serve the folder with any
static server (e.g. `npx serve .`).

## Use it inside HighLevel AI Studio

**AI Studio** is HighLevel's built-in app & website builder (enable it under
HighLevel Labs in your sub-account). In October 2026 AI Studio gained
**two-way GitHub sync**, which is exactly what this repo is for:

1. In HighLevel, open **AI Studio** and create (or open) a project.
2. In the project's **settings**, connect your GitHub account.
3. Link this repository — code now syncs **both ways** between AI Studio and
   GitHub (with secret scanning on pushes), so edits made here show up in the
   AI Studio project and vice versa.
4. From there the calculator can sit inside the client's HighLevel account —
   wired to the CRM, calendars and workflows like any AI Studio app.

Prefer to iterate outside HighLevel? The same repo opens in any editor or AI
coding tool; push, and AI Studio pulls the changes in on sync.

## The math (verified against the deck)

- Hours back/mo = round(hours × % × accounts × 52/12)
- Value/mo = hours back × rate · Stack/mo = (HighLevel plan + Muse) × accounts
- Net/mo = value − stack · Annual net = net × 12 · Payback ≈ stack ÷ (value/30), rounded up to days
- Checkpoints: defaults (10 hrs, $75, 60%, 1 account, $97) → **26 hrs back, $1,950 value, $1,853 net, $22,236/yr**.
  At 5 accounts → **130 hrs back, $9,750 value, $9,265 net, $111,180/yr**.

## Credit

Built for the HighLevel Dallas Chapter monthly meeting (Oct 22, 2026) by
**Hivergent AI**. Mascot: the Muse star-bot, drawn as inline SVG so the app
stays a single self-contained file — no build step, no image assets.
