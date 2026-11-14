# Continence Tracker

Continence Tracker is a small, responsive web app for recording pad weights and tracking changes in urinary leakage over time. It runs from a single `index.html` file, without an account, database, or server-side application.

## Features

- Create pad types with a name and default **dry weight** (grams).
- Record a **date**, **pad type**, **dry weight**, and **wet weight** for each used pad. You can override the dry weight for an individual measurement.
- Automatically calculate **net weight = wet weight − dry weight**.
- Record multiple pads on the same date; the app sums their net weights for that date.
- See average **daily net weight** over the last **7, 14, and 28 calendar days**.
- Edit or delete measurements and archive/reactivate pad types.
- Export a complete **JSON backup**, restore it, or export measurements as **CSV**.
- Use the same interface on a phone, tablet, or desktop browser.

## How averages work

Each window includes today and the preceding 6, 13, or 27 days, respectively. The app adds the net weights of all pads for each recorded date, then divides the sum of those daily totals by the number of days **with entries** in that window. Days with no entries are **excluded** rather than assumed to have zero leakage. The dashboard displays the number of recorded days, for example `3 of 7 days recorded`.

Net pad weight is measured in grams; it can provide an approximate indication of leakage volume, but moisture other than urine may affect measurements. This app is a personal tracking tool, not a medical device or diagnostic tool.

## Where data lives

Measurements and pad profiles are stored using browser `localStorage` under the key `continence-tracker-v1`. Data is kept separately for each browser and website origin, and does **not** sync between devices or browsers. The app does not upload measurements to GitHub or a remote database.

Stored records may be lost when browser website data is cleared, a browser/profile is removed, or local-file storage is reset. Private browsing is not appropriate for durable record keeping. Regular JSON backups are strongly recommended.

## Back up and restore

Open **Backup & data**:

- **Export backup (JSON)**: downloads a file containing measurements and pad-type settings. Save it in a location you control.
- **Restore backup (JSON)**: selects a previously exported JSON file. **Warning: restore replaces all current measurements and pad profiles** in that browser after confirmation. Export a backup of current data first if you need it.
- **Export history (CSV)**: creates a spreadsheet-compatible list of entries for analysis. **CSV cannot be used for Restore backup.**

Treat backups as personal health-related information and store/share them accordingly. The app does not encrypt the exported files.

## Project files

- `index.html` — complete app (HTML, CSS, JavaScript in one file)
- `README.md` — project overview and technical/setup notes
- `HOW_TO_USE.md` — daily-use instructions

## Limitations

- The app does not sync data automatically across browsers or devices.
- It does not distinguish daytime/nighttime data unless you select appropriately named pad types.
- A day with only some pads entered is treated as a recorded day; for meaningful daily averages, enter **all pads used** that day.
- Changes to a pad type's default dry weight do not rewrite previously saved measurement weights.
