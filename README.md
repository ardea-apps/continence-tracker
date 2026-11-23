# Continence Tracker v1.3.3

A standalone, mobile-friendly HTML application for tracking urinary leakage using individual dry and wet pad weights. No account, server, database, external library or network API is required.

## Features

- When no pad is active, the main screen shows **Start New Pad**. Enter the actual dry weight, select Day/Night, and select **Start Pad**.
- When a pad is active, the same area shows **Close Current Pad**. Enter the actual wet weight and select **Close Pad**.
- After closing, the completed entry is saved to History and the **Start New Pad** form appears immediately, with no intermediate confirmation or page navigation. The app remembers which state it is in when reopened.
- Enter historical completed measurements manually; edit or delete them later.
- Edit or discard an active measurement.
- Day/Night classification, with a suggested opposite period for the next pad (editable).
- Collapsible History grouped by removal date; daily totals and expandable details.
- Daily totals and rolling 7-, 14- and 28-day averages, each with a small Day/Night breakdown and an indication of unclassified measurements.
- JSON backup and restore, including active measurements; CSV export of completed measurements.
- Compatible with existing version 1.0 data and JSON backups.

## Calculations

Net weight = wet weight − dry weight, in grams. Each pad is weighed individually; no pad profiles or default weights are needed. All of a completed pad's net weight belongs to its removal date (including when use spans midnight). Daily totals sum all completed measurements for that date. Rolling averages use the preceding 7, 14 or 28 completed local calendar days, ending yesterday, dividing by the number of dates with completed measurements. Today is excluded until the next calendar day but remains visible in History. Each rolling-average card also shows Day and Night leakage per recorded calendar day, using the same denominator as the overall average. A date with at least one completed pad counts once, even if a Day or Night pad is absent. An absent classification contributes zero to that component, not an inferred amount. Unclassified measurements remain in the overall average, and the card displays an Other amount when they occur. Missing dates are excluded, not zero; past dates with incomplete records contribute only their recorded amount. Active measurements do not contribute. Pad-weight gain is a proxy for leakage and may include other moisture.

## Running and publishing

Open `index.html` in a modern browser for local testing. Browser storage for local files varies by browser. For consistent use, host the app on GitHub Pages.

1. Create the `continence-tracker` repository under `ardea-apps` (or use the existing repository).
2. Upload `index.html`, the icon assets, `README.md` and `HOW_TO_USE.md` to the repository root.
3. In Settings → Pages, deploy from the main branch, root folder.
4. Open the resulting Pages URL, or `https://ardea-apps.garcez.net/continence-tracker/` if that custom domain is configured.
5. Do not list this personal app on the public apps index if you prefer an unlisted link. An unlisted URL is not access control.

Works with modern desktop and mobile browsers. On iPhone, Safari's Share → Add to Home Screen can provide convenient access with the included Apple touch icon; verify storage and restore a backup if the home-screen app starts with empty data.

## Release v1.3.3 changes

Added Day and Night component averages under each existing 7-, 14- and 28-day average, using only sun and moon icons without redundant text labels. The combined daily average and completed-day windows are unchanged. Unclassified historical measurements continue to appear as an Other component when applicable. No changes were made to stored data, the export/restore schema, measurement workflow or Home Screen icons.

## Backup filenames

JSON backups use a timestamped filename in local time, in the format `continence-tracker-backup-YYYY-MM-DD_HHMMSS.json` (for example, `continence-tracker-backup-2026-11-21_143527.json`). This allows multiple backups on the same day to have different names. The timestamp changes the filename only, not the backup contents or restore procedure. Older JSON backups remain supported. Backups are ordinary, unencrypted files; save them securely.

## Storage and privacy

All measurements are kept in browser localStorage under the existing key `continence-tracker-v1`. GitHub hosts code only. Each browser/device/origin maintains its own dataset. There is no automatic synchronization. Local file and hosted storage are separate. Clearing website data or browser storage may erase records. JSON/CSV files are not encrypted; keep them in a secure location and never commit personal data to GitHub. Other scripts on the same web origin may have access to browser storage; local storage is not a security boundary between apps on that origin.

## Upgrade from v1.0 or v1.1

Export a JSON backup before replacing the HTML. Version 1.3.4 reads the existing storage key and accepts backup schemas 1, 2 and 3. Existing completed and active measurements retain their weights, dates and timestamps; missing Day/Night classifications remain unclassified until edited. Old pad names are preserved where available. New backups use schema 3 to preserve the period field; older versions cannot read them. Rolling averages exclude the current calendar day. Version 1.3.4 uses a single adaptive main screen: close the current pad first, then start a replacement. It also places this workflow above the averages. The stored data format is unchanged.

When moving from a local file to the hosted app or between devices, export a backup from the source browser, open the destination app and restore it. Restore replaces the destination dataset, not merges it. Use one primary device to avoid conflicting records.

See [HOW_TO_USE.md](HOW_TO_USE.md) for the daily workflow.

## Release files

`continence-tracker-v1.3.3.html` and `index.html` are identical. Use the versioned file for archiving and `index.html` for deployment.
