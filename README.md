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

## Medication Schedule

- เช้า: Methylphenidate 10 mg x 2, Fluoxetine 20 mg x 2, Propranolol 10 mg x 1, Naproxen 250 mg x 1, Nurtec 75 mg x 1 วันเว้นวัน.
- กลางวัน: Methylphenidate 10 mg x 2.
- เย็น: Methylphenidate 10 mg x 2, Propranolol 10 mg x 1, Naproxen 250 mg x 1.
- ก่อนนอน: Pregabalin 75 mg x 1, Amitriptyline 25 mg x 1, Flunarizine 5 mg x 1.

Special rules:
- Nurtec shows last taken and next scheduled dose automatically.
- Naproxen has an editable start date. First 3 days are morning/evening; after that the UI shows every-12-hour timing.
- Propranolol is morning and evening only.

## Run

Open `index.html` in a browser. Data is stored locally in `localStorage`.
