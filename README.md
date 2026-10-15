# StudySprint — Exam Countdown & Study Planner

**Tagline:** Count down to your board exams, master every chapter, and study with focus — all in one beautiful planner.

**Live:** https://abhiramunni.github.io/studysprint/

## What it does

StudySprint is a single-page web app for students preparing for board exams (Class 10, Class 12, or any exam). It combines four tools students otherwise juggle across notebooks and apps:

- **Exam countdowns** — add any exam with its date; a live ticking countdown (days / hours / minutes / seconds) with a progress ring keeps the deadline real. Supports multiple exams (prelims + boards).
- **Subject & chapter tracker** — break each subject into chapters, tick them off, and watch per-subject progress bars and an overall syllabus-completion stat grow.
- **Daily study planner** — plan today's tasks (topic + subject + minutes) and check them off.
- **Pomodoro focus timer** — 25-minute focus / 5-minute break sessions (customizable) with an animated ring timer. Finished sessions log minutes automatically.
- **Streaks, stats & revision queue** — day streaks, chapters completed, focus hours, a 7-day minutes chart, and a revision queue for chapters flagged "needs revision".

## Who it's for

School and college students, **and their parents** — plain-language helpers throughout plus a "Note for parents" card explaining streaks, chapters, focus hours and the revision queue. No sign-up, no jargon.

## Design — "Academia" v2 (Oct 2026 redesign)

- **Palette:** warm ivory paper (`#FAF6EE`), espresso ink (`#241A10`), burnt amber/bronze (`#A85B12`), terracotta clay (`#9C3A1E`), gold (`#D9A441`). Professional, warm, print-like — deliberately not a flat violet/green/blue theme.
- **Typography:** Fraunces (serif display) + Inter (UI).
- **Cinematic full-screen intro:** espresso backdrop, rising gold-dust canvas particles, stroke-drawn book logo, staggered title letters, progress bar, tap-to-skip. Full version on first launch, quick version on return visits.
- **Aesthetic study photography** with slow Ken Burns drift for video-like motion (real video generation is region-blocked): golden-hour study desk hero, note-writing close-up, grand library hall — in `assets/`.
- Motion: motion-one entrance springs, breathing timer halo, animated progress rings/bars; `prefers-reduced-motion` respected throughout.
- Zero emojis — hand-drawn inline SVG icon set throughout.

## How to use

1. Open the app — the cinematic intro plays, then a 3-step welcome tour explains the flow (or skip it).
2. **Exams tab:** type an exam name (e.g. "Class 12 Boards"), pick its date, tap **Add exam**. The countdown starts ticking immediately.
3. **Study tab:** add a subject (pick a colour), then add its chapters one by one. Tick chapters off as you finish them. Flag shaky chapters with the circular-arrow button to send them to the revision queue.
4. Still in **Study tab:** add today's tasks — what you'll study, which subject, how many minutes. Check them off when done; each completed task keeps your streak alive.
5. **Focus tab:** tap **Start** for a 25-minute focus session. When it ends, the minutes are logged and a break begins. Adjust durations with the Focus/Break inputs.
6. **Stats tab:** see your streak, totals, the 7-day chart, and clear your revision queue.

## Tech stack

- `index.html` — the whole app (HTML, CSS, vanilla JS); `assets/` holds the three study photographs
- [Motion One](https://motion.dev/) (CDN) for spring animations and staggered entrances
- [Fraunces](https://fonts.google.com/specimen/Fraunces) + [Inter](https://fonts.google.com/specimen/Inter) (Google Fonts CDN)
- SVG for icons, progress rings, and charts

## Data & privacy

- All data (exams, subjects, chapters, tasks, sessions, streak) is stored in your browser's `localStorage` under the key `studysprint_v1`. Nothing is sent to any server.
- The app works fully offline after first load (except the font/animation CDNs, which degrade gracefully).
- Clearing browser site data erases your StudySprint data.

Built by [Abhiram Unni](https://github.com/abhiramunni) as part of a daily shipping streak.
