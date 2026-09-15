# Project Budget Tracker

A classroom build-challenge budget tracker from The Holler. Teachers or Holler
technicians set a budget and stock a "supply depot"; students tap to shop from a
shared touchscreen and watch their funds drop live. Every purchase is timestamped
for a spending-over-time chart and an exportable log.

The whole tool is **one file: `index.html`.** No server, no accounts, no internet
required once it's open.

## Put it on theholler.org

1. Upload `index.html` anywhere that serves static files (a GitHub Pages repo like
   Paper Scrubber, or a folder on theholler.org) and link to it from the Tools page.
   To embed it in the page instead of opening in a new tab:
   ```html
   <iframe src="https://YOUR-URL/index.html" style="width:100%;height:90vh;border:0;border-radius:12px"></iframe>
   ```
2. Visitors can grab their own copy with the **Download a copy** button on the
   projects page. It saves the entire tool as `project-budget-tracker.html`, which
   runs from a laptop, a classroom computer, or a USB drive with no internet and
   keeps its own saved projects.
3. To publish an update, replace `index.html`. That's it.

Suggested blurb for the Tools page:

> **Project Budget Tracker** — set a budget, stock a supply depot, and watch every
> team's spending live. [Open the tool](https://YOUR-URL/) or download it from
> inside the tool to run offline. Works on touchscreens, saves your projects on the
> device, no account needed.

## Branding

The tool carries The Holler's branding: the wordmark in the header and footer, the
H mark as the browser-tab icon, and a palette sampled from the official logo
(Holler yellow `#F9CB4E` on buttons and highlights with dark text, deep Holler amber
`#9C6D14` for prices and links so they stay readable). The logo images are embedded
in the file, so they show even offline. To adjust anything, edit the
**BRAND TOKENS** block at the top of the `<style>` section.

## How saving works

- Projects auto-save on every tap to the browser's local storage **on that device**
  (the "Saved 2:41 PM" note in the header confirms each save).
- Close the tab, come back next week, and the project is still there.
- Local storage is per device and per browser. To move a project to another
  computer or back it up, use **Export** (downloads a `.budget.json`) and
  **Import project file** on the other machine.
- Private/incognito windows and some locked-down school browsers block storage.
  The app warns you with a banner when that happens; export before closing.
- **Duplicate** copies a project's setup (challenges, materials, teams, rules) with a
  clean slate for purchases. **Reset purchases** (on the project board) clears every
  purchase in place. It and Delete project both ask you to type a word (CLEAR /
  DELETE) first, so a stray tap on a shared screen can't wipe a class's work.

## Starting a project

**New project** walks through a short setup:

1. Name and money symbol ($, § mission funds, ¢, points, €, £, or a custom symbol).
2. Tick one or more **challenges**. Each gets its own stocked depot. Tick one for a
   single build, several for a multi-challenge day. Once a challenge is ticked, open
   its **Materials** list to untick anything you don't want in the depot (no balloons,
   no hot glue, and so on) before the project is created. Add blank challenges if you
   want to stock your own.
3. If you picked more than one challenge, choose **one combined budget** for the whole
   project or a **separate budget per challenge** (optionally carrying leftovers forward).
4. Optional: efficiency bonus scoring and the low-funds warning level.

Challenge presets included: Egg Drop Lander, Bridge Build, Tallest Tower, Earthquake
Shelter, Paper Glider, Parachute Drop, Cargo Boat, Balloon-Powered Car, Catapult
Launch, Marble Run, Wind Turbine, Water Filter. Prices are on a ~100-per-team
scale so any single challenge works out of the box; edit anything in **Materials**.

You can also add a challenge to an existing project later: **Settings → Add a challenge…**

## Running a multi-challenge day

The project board shows **Challenge 1 of N** with the challenge list underneath.
Tap **Next challenge** when the class moves on. Shopping switches to that
challenge's depot; with a combined budget, teams keep spending from the same pool.
Tap any challenge in the list to look back at it.

## Free lesson plans

Every challenge preset links to a free, no-login lesson plan or activity guide
(shown on the setup card, the project board, and the Materials dialog):

| Challenge | Source |
|---|---|
| Egg Drop Lander | TeachEngineering — *Egg-cellent Landing* (students build to a budget) |
| Bridge Build | TeachEngineering — *Operation Build a Bridge and Get Over It* |
| Tallest Tower | TeachEngineering — *Leaning Tower of Pasta* |
| Earthquake Shelter | TeachEngineering — *Shake It Up! Engineering for Seismic Waves* |
| Paper Glider | TeachEngineering — *Paper Airplanes: Building, Testing, & Improving* |
| Parachute Drop | TeachEngineering — *Design a Parachute* |
| Cargo Boat | Science Buddies — *How Much Weight Can Aluminum Foil Boats Float?* |
| Balloon-Powered Car | Science Buddies — *Balloon Car Lesson Plan* |
| Catapult Launch | Science Buddies — *Build a Popsicle Stick Catapult* |
| Marble Run | Science Buddies — *Build a Paper Roller Coaster* |
| Wind Turbine | TryEngineering (IEEE) — *Working with Wind Energy* (teams buy materials on a budget) |
| Water Filter | TeachEngineering — *Water Filtration Project* (filtered water earns $ by grade) |

Three hubs worth bookmarking for anything else: **teachengineering.org** (K-12,
NGSS-aligned, thousands of free activities), **sciencebuddies.org/teacher-resources**
(free lesson plans; a free account is only needed to assign them to students), and
**tryengineering.org** (IEEE's free lesson plans, several built around a materials budget).
