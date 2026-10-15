# StudySprint — Exam Countdown & Study Planner

**Tagline:** Count down to your board exams, master every chapter, and study with focus — all in one beautiful planner.

## What it does

StudySprint is a single-page web app built for students preparing for board exams (Class 10, Class 12, or any exam). It combines four tools students otherwise juggle across notebooks and apps:

- **Exam countdowns** — add any exam with its date; a live ticking countdown (days / hours / minutes / seconds) with a progress ring keeps the deadline real. Supports multiple exams (prelims + boards).
- **Subject & chapter tracker** — break each subject into chapters, tick them off, and watch per-subject progress bars and an overall syllabus-completion stat grow.
- **Daily study planner** — plan today's tasks (topic + subject + minutes) and check them off.
- **Pomodoro focus timer** — 25-minute focus / 5-minute break sessions (customizable) with an animated ring timer. Finished sessions log minutes automatically.
- **Streaks, stats & revision queue** — day streaks, chapters completed, focus hours, a 7-day minutes chart, and a revision queue for chapters flagged "needs revision".

## Who it's for

School and college students (especially Class 10/12 board aspirants), and anyone preparing for a dated exam who wants structure without signing up for anything.

## Features

- Live per-second exam countdowns with progress rings and plain-words nudges ("Tomorrow! Light revision only.")
- Subjects with custom colours, chapter checklists, and animated progress bars
- Today's task list with minutes estimates
- Pomodoro timer: focus/break modes, start / pause / resume / reset, session counter, custom durations
- Streak tracking (a day counts when you finish a task or a focus session)
- Stats dashboard: streak, chapters done, focus hours, syllabus %, 7-day minutes bar chart
- Revision queue with "Revise today" flags and one-tap completion
- 3-step first-run onboarding, helper text, tooltips, friendly empty states
- Fully responsive mobile-first design; respects `prefers-reduced-motion`
- Zero emojis — hand-drawn inline SVG icon set throughout

## How to use

1. Open the app. The 3-step welcome tour explains the flow (or skip it).
2. **Exams tab:** type an exam name (e.g. "Class 12 Boards"), pick its date, tap **Add exam**. The countdown starts ticking immediately.
3. **Study tab:** add a subject (pick a colour), then add its chapters one by one. Tick chapters off as you finish them. Flag shaky chapters with the circular-arrow button to send them to the revision queue.
4. Still in **Study tab:** add today's tasks — what you'll study, which subject, how many minutes. Check them off when done; each completed task keeps your streak alive.
5. **Focus tab:** tap **Start** for a 25-minute focus session. When it ends, the minutes are logged and a break begins. Adjust durations with the Focus/Break inputs.
6. **Stats tab:** see your streak, totals, the 7-day chart, and clear your revision queue.

## Tech stack

- Single self-contained `index.html` — HTML, CSS, and vanilla JavaScript inline
- [Motion One](https://motion.dev/) (CDN) for spring animations, staggered entrances, and count-ups
- [Inter](https://fonts.google.com/specimen/Inter) typeface (Google Fonts CDN)
- SVG for all icons, progress rings, gauges, and charts — no image assets

## Live demo

https://abhiramunni.github.io/studysprint/

## Data & privacy

- All data (exams, subjects, chapters, tasks, sessions, streak) is stored in your browser's `localStorage` under the key `studysprint_v1`. Nothing is sent to any server.
- The app works fully offline after first load (except the font/animation CDNs, which degrade gracefully).
- Clearing browser site data erases your StudySprint data.

Built by [Abhiram Unni](https://github.com/abhiramunni) as part of a daily shipping streak.
