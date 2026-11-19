# MyLife — Your Personal Life Dashboard

MyLife is a private, local-first dashboard for daily journaling, health tracking, studies, Lumiweb business records, personal finances, and planning.

## Features

- Dashboard summaries and a weekly journal chart based on saved records.
- Daily mood, ratings, and editable habit tracking.
- Health records for weight, meals, water, activity, workouts, sleep, and cycle dates.
- Study subjects, grades, assignments, exams, and study sessions.
- Lumiweb projects, clients, orders, tasks, business transactions, and portfolio links.
- Personal income, expenses, savings goals, budgets, and an event calendar.
- Weekly/monthly review summaries, global search, five themes, JSON backup/restore, and CSV export.
- Optional sample data that is marked and can be removed separately.

## Project structure

```text
index.html       App shell and external Chart.js include
styles.css       Responsive visual design and themes
js/store.js      Versioned LocalStorage data model and validation
js/schema.js     Navigation and reusable record schemas
js/charts.js     Chart.js rendering from saved records
js/app.js        Navigation, forms, page views, and app interactions
```

## Run locally

Open the folder in VS Code and launch `index.html` with the Live Server extension. The app uses ES modules, so use a local HTTP server rather than opening the file directly.

## LocalStorage and backups

All records are stored automatically in this browser's LocalStorage under `mylife.workspace.v1`. LocalStorage is tied to the current browser and device; it does not synchronize between devices. Export a JSON backup regularly from Settings. To restore, choose a MyLife JSON backup; the app validates it and asks before replacing current data. CSV exports are available for finance, grades, and journal/habit records.

Chart.js and the optional fonts are loaded from CDNs; an internet connection is needed for those external assets. Core data entry and navigation are local.
