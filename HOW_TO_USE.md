# Continence Tracker — How to use

## 1. Start a new pad

1. Weigh the actual dry pad before putting it on.
2. Open Continence Tracker and enter its dry weight in grams.
3. Check the automatically populated start date and time; change them if necessary.
4. Select **Start measurement**. The active measurement is saved in this browser, even if you close the app.

## 2. Change your pad

When you remove the old pad and put on a new one:

1. Weigh the used pad and the new dry pad separately.
2. Open the app. The saved dry weight of the old pad is displayed.
3. Check the removal date and time (defaults to current local time).
4. Enter the old pad's wet weight and the new pad's actual dry weight.
5. Select **Complete & start new**. The old measurement is saved and the next one starts at the removal time.

If you are not putting on another pad, leave the new dry weight blank and select **Complete only**. Use **Edit active pad** to correct a dry weight or start time, or **Discard active pad** followed by confirmation to remove an unfinished entry.

Example: A pad weighed 18 g dry and 26 g wet. Its recorded net weight is 8 g. A new pad weighing 21 g dry starts its own independent measurement. No preset pad weights are used.

## 3. Read your results

The 7-, 14- and 28-day averages represent grams per recorded day, including today. The history shows individual measurements and each date's total. A pad started at night and removed the following morning belongs entirely to the morning's date. Active pads are not counted. Missing dates are excluded; an explicitly recorded zero is counted. A day with only part of its measurements recorded contributes only the recorded amount.

If wet weight is less than dry weight, recheck the measurements. The app does not accept a negative net weight.

## 4. Enter or correct historical data

Open **Add completed measurement manually**. Enter removal date and both actual weights. Start date/time and removal time are optional. Save. For corrections select **Edit** beside a history entry, then **Update measurement**. To delete, tap **Delete measurement**, then **Confirm delete**. Cancel edit to abandon unsaved changes.

## 5. Backup and restore

Open **Backup & data** and select **Export backup (JSON)**. Save the file in a secure folder (on iPhone, Files is one option). It contains all completed measurements and any active measurement. Export regularly and before upgrading, changing devices or clearing browser data.

To restore, select **Restore backup (JSON)**, choose the file, review the entry count, then select **Replace current data**. This replaces the entire current dataset. Export the destination's existing data first if you need to retain it. Version 1.0 backups can be imported; historical pad measurements are preserved, but pad profiles are no longer used.

**Export history (CSV)** saves completed measurements for spreadsheet analysis; it is not a restorable backup.

## 6. Using multiple devices

The app works in modern desktop and mobile browsers. The hosted app code is on GitHub Pages, but measurements are local to each browser/device. No automatic synchronization occurs. To move from local testing to the hosted app (even on the same device), export JSON from the local copy and restore into the hosted copy. Transfer backups between devices only when desired; do not upload backups to GitHub. Keep one primary data-entry device to avoid conflicting records.
