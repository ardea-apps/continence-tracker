# Continence Tracker v1.3 — How to use

## 1. Start a new pad (when none is active)

1. Weigh the actual dry pad before putting it on.
2. Open Continence Tracker and enter its dry weight in grams and select Day or Night.
3. Check the automatically populated start date and time; change them if necessary.
4. Select **Start Pad**. The active measurement is saved in this browser, even if you close the app.

## 2. Close the current pad, then start the next one

**First: complete the used pad.**

1. Remove the current pad and weigh it wet.
2. Open the app. The active pad’s saved dry weight is shown.
3. Check the removal date and time (defaults to now).
4. Enter the used pad’s wet weight and tap **Close Pad**.
5. The completed measurement is saved immediately and appears in History under the removal date. The app immediately switches to **Start New Pad**, with no separate page or confirmation.

**Next: start the replacement pad.**

1. Weigh the new pad dry.
2. On the **Start New Pad** screen, check the Day/Night selection and start date/time.
3. Enter its actual dry weight and tap **Start Pad**.

You can leave the app after completing the old pad and return later to start another. You cannot accidentally overwrite the completed pad by abandoning the second step.

If you are not putting on another pad, simply stop after **Close Pad**. Use **Edit active pad** to correct the current pad’s dry weight, start time or period, or **Discard active pad**, then confirmation, to remove an unfinished entry.

Example: A pad weighs 18 g dry and 26 g wet. Complete it to record 8 g net. Then start a separate measurement for a replacement pad weighing 21 g dry. No preset pad weights are used.

## 3. Read your results

The 7-, 14- and 28-day averages represent grams per recorded day, using the preceding 7, 14 or 28 completed local calendar days, ending yesterday. Today is visible in History but does not affect averages until tomorrow. History is collapsed by default. Expand **History** to see daily totals, newest first. Expand an individual date to see its measurements, Day/Night classification and Edit buttons. A pad started at night and removed the following morning belongs entirely to the morning's date. Active pads are not counted. Missing dates are excluded; an explicitly recorded zero is counted. A past day with only part of its measurements recorded contributes only the recorded amount.

If wet weight is less than dry weight, recheck the measurements. The app does not accept a negative net weight.

## 4. Enter or correct historical data

Expand **History**, then open **Add completed measurement manually**. Enter removal date, both actual weights, and Day/Night if known. Start date/time and removal time are optional. Save. For corrections select **Edit** beside a history entry, then **Update measurement**. To delete, tap **Delete measurement**, then **Confirm delete**. Cancel edit to abandon unsaved changes.

## 5. Backup and restore

Open **Backup & data** and select **Export backup (JSON)**. Save the file in a secure folder (on iPhone, Files is one option). It contains all completed measurements and any active measurement. Export regularly and before upgrading, changing devices or clearing browser data.

To restore, select **Restore backup (JSON)**, choose the file, review the entry count, then select **Replace current data**. This replaces the entire current dataset. Export the destination's existing data first if you need to retain it. Version 1.0 and 1.1 backups can be imported. Existing measurements remain unclassified unless a period was already saved. Assign Day/Night through Edit if desired. Version 1.2.2 backups include Day/Night for completed and active measurements; older apps cannot read the new schema.

**Export history (CSV)** saves completed measurements for spreadsheet analysis; it includes the Day/Night period and is not a restorable backup.

## 6. Using multiple devices

The app works in modern desktop and mobile browsers. The hosted app code is on GitHub Pages, but measurements are local to each browser/device. No automatic synchronization occurs. To move from local testing to the hosted app (even on the same device), export JSON from the local copy and restore into the hosted copy. Transfer backups between devices only when desired; do not upload backups to GitHub. Keep one primary data-entry device to avoid conflicting records.
