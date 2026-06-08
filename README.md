# Migraine Journal

A personal-first migraine journal for one user. It is optimized for logging during severe migraine: large buttons, dark mode, minimal typing, local-first storage, and fast medication/prodrome/attack capture.

## Goals

- One tap medication logging with automatic timestamps.
- Prodrome and attack logging with large buttons.
- Improvement logging with attack duration and medication-to-improvement timing.
- Sleep tracking stored separately for future Apple Watch integration.
- Local health calendar for doctor appointments and medication refill dates.
- Neurologist report with clinical translation.
- Manual Files/iCloud Drive backup and import for iPhone PWA use.

## Core Flows

- `วันนี้`: urgent actions and today's timeline.
- `ยา`: 💊 กินยาแล้ว, missed meds, adherence, and today's med history.
- `ไทม์ไลน์`: all migraine, sleep, and medication events.
- `ปฏิทิน`: นัดหมอ and สั่งยา / รับยา.
- `รายงาน`: neurologist summary.

## Backup / Import

- Export creates a JSON backup named `migraine_data_YYYY-MM-DD.json`.
- Save that file manually to Files / iCloud Drive.
- Import uses an HTML `.json` file picker. The user must choose the backup file manually.
- If local data already exists, the app asks whether to replace, merge, or cancel.
- Imported data is copied into `localStorage`, so the app keeps working offline.
- The app shows `ยังไม่ได้ backup วันนี้` if there has been no export in 24 hours.

There is no server, login, or fake automatic iCloud sync. Browser/PWA file access on iPhone requires user selection.

## Run

Open `index.html` in a browser. Data is stored locally in `localStorage`.
