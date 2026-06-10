# Migraine Journal

Personal migraine and sleep log PWA for one person. Optimized for fast iPhone logging during migraine symptoms.

Live app:

https://afaitz19.github.io/migrainesleeplogs/

Version: Version 2, updated 10-06-2026.

## iPhone Setup

1. Open the live app URL in Safari.
2. Tap Share.
3. Tap Add to Home Screen.
4. Use the Home Screen icon like an app.

Do not open the local `file://` HTML file on iPhone. iPhone Safari/PWA works much better from the GitHub Pages web URL.

## Core Flows

- `วันนี้`: urgent actions and today's timeline.
- `ยา`: medication logging, missed meds, adherence, and today's med history.
- `ไทม์ไลน์`: graph-based migraine pattern view plus detailed event cards.
- `ปฏิทิน`: doctor appointments and medication refill dates.
- `รายงาน`: neurologist-readable clinical dashboard.

## Backup / Import

- Export creates a JSON backup named `migraine_data_YYYY-MM-DD.json`.
- Save that file manually to Files / iCloud Drive.
- Import uses an HTML `.json` file picker. The user must choose the backup file manually.
- If local data already exists, the app asks whether to replace, merge, or cancel.
- Imported data is copied into `localStorage`, so the app keeps working offline.
- There is no server, login, or fake automatic iCloud sync.

## Medication Schedule

- เช้า: Methylphenidate 10 mg x 2, Fluoxetine 20 mg x 2, Propranolol 10 mg x 1, Naproxen 250 mg x 1, Nurtec 75 mg x 1 วันเว้นวัน.
- กลางวัน: Methylphenidate 10 mg x 2.
- เย็น: Methylphenidate 10 mg x 2, Propranolol 10 mg x 1, Naproxen 250 mg x 1.
- ก่อนนอน: Pregabalin 75 mg x 1, Amitriptyline 25 mg x 1, Flunarizine 5 mg x 1.

Special rules:

- Nurtec shows last taken and next scheduled dose automatically.
- Naproxen has an editable start date. First 3 days are morning/evening; after that the UI shows every-12-hour timing.
- Propranolol is morning and evening only.

## GitHub Pages

This repository includes a static `index.html`, `.nojekyll`, and a GitHub Actions Pages workflow. If the live URL does not work yet, open repository Settings, then Pages, and set the source to GitHub Actions.
