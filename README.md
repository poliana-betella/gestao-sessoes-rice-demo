# Team Time Tracker — Notion Portfolio Demo

A time-tracking and team-metrics system built in Notion for a small data team, rebuilt from scratch as a portfolio piece.

**Live demo (Notion):** https://safe-stallion-dd4.notion.site/Team-Time-Tracker-Portfolio-Demo-3de0bf7d46d3804f9c72ee0ff126f62a

The published page can be duplicated as a template (Duplicate button, top right).

> All names, projects and numbers are fictional. No real company, client or personal data is used.

## What it does

- **Work sessions with pause and resume.** Each session has three buttons: **Start / Resume**, **Pause** and **Complete**. Only active time is counted; paused time is never billed.
- **Automatic metrics.** Worked hours and cost (active minutes × the member's hourly rate) are formulas that roll up to projects and team members.
- **RICE prioritization vs. real effort.** Projects are scored with RICE (Reach × Impact × Confidence ÷ Effort) using the *estimated* effort, and compared with the effort actually tracked ("84% of estimate", "124% of estimate").

## Data model

| Database | Key properties |
|---|---|
| **Work Sessions** | Session, Project (relation), Member (relation), Activity, Status, Started, Ended, Last Resumed, Accumulated Min, Pauses, Worked Hours, Duration, Cost, buttons |
| **Projects** | Status, Squad, Reach, Impact, Confidence, Estimated Hours, RICE Score, Logged Hours, Total Cost, Effort vs Estimate, Team Size |
| **Team** | Role, Squad, Hourly Rate, Logged Hours, Total Cost, Projects |

## How the timer works

| Button | What it changes |
|---|---|
| Start / Resume | Status → Running, Last Resumed → now, Started → now (only on the first click) |
| Pause | Accumulated Min += minutes since Last Resumed, Pauses += 1, Status → Paused |
| Complete | Accumulated Min += minutes since Last Resumed (if running), Status → Done, Ended → now |

Worked Hours = (Accumulated Min + live minutes if running) ÷ 60

## Views

Active sessions · Projects by RICE · Team metrics · Session log grouped by project (with sums)

## Tools

Notion databases, relations, Formulas 2.0 and button automations.
