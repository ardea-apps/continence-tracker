# How to Use Continence Tracker

Continence Tracker records the dry and used weight of each pad, calculates the difference, and shows average daily leakage over 7, 14, and 28 days. It works in a modern browser on iPhone, Android, Windows, macOS, or Linux.

## 1. Set up your pad types (once)

1. Open **Pad types & settings**.
2. Enter a name, such as **Day Pad** or **Night Pad**.
3. Weigh a new, unused pad and enter its **Default dry weight (g)**.
4. Tap **Add pad type**.
5. Repeat for other pad types.

When you change brands or models, add a new pad type. You can edit an existing profile or archive one you no longer use. Changing a profile's default weight does **not** change older saved measurements.

## 2. Record a used pad

1. Go to **Add measurement**.
2. Select the **date** (today is preselected).
3. Choose the **pad type**. Its saved dry weight appears automatically.
4. Adjust **Dry weight (g)** if this particular unused pad has a different dry weight.
5. Weigh the used pad and enter **Wet weight (g)**.
6. Check the displayed **Net weight**, which is the wet weight minus the dry weight.
7. Tap **Save measurement**.

**Example:** Dry 26 g, wet 34 g → net 8 g.

Add **one measurement for each pad used**. For instance, enter a daytime pad and a nighttime pad separately on the same date. Use the correct date for each measurement consistently.

## 3. Understand the averages

The three cards at the top show **average daily net weight** for the last 7, 14, and 28 calendar days, including today.

- If two pads on the same date have net weights of 8 g and 14 g, that day's total is **22 g**.
- Days without any measurements are **not** counted as zero. Instead, the app averages across days with at least one measurement.
- Check the note beneath each average (such as **1 of 7 days recorded**) before interpreting the result.

For the most meaningful averages, enter all pads for each day. If you have not finished entering today's pads, today's total—and the displayed averages—are still provisional.

## 4. Correct or delete a measurement

1. In **History**, find the measurement and tap **Edit**.
2. Update its fields and tap **Update measurement**, or choose **Cancel edit**.
3. To remove it, tap **Delete measurement** and then **Confirm delete**. The second tap permanently deletes that measurement.

The history and averages recalculate after changes.

## 5. Back up your data

Make a backup regularly, especially before clearing browser history/website data, changing phones, or switching from a local HTML file to GitHub Pages.

1. Expand **Backup & data**.
2. Tap **Export backup (JSON)**.
3. Save the downloaded `.json` file somewhere safe, such as your preferred folder in the Files app.

The JSON backup includes measurements **and** pad settings. **Export history (CSV)** is useful for a spreadsheet, but it is **not** a restorable backup.

## 6. Restore a backup

1. On the browser/device where you want the data, open **Backup & data**.
2. Tap **Restore backup (JSON)** and select the saved `.json` file.
3. Read the confirmation: **restoring replaces all existing measurements and pad profiles in that browser**.
4. Confirm only if you want to replace its current records.

If you have measurements on both devices, back up both first. Restore does not merge two databases.

## 7. Move from the local file to GitHub Pages

Because you're testing `index.html` locally before publishing it, follow these steps when you're ready:

1. In the **local** app, use **Export backup (JSON)** and save the file.
2. Publish `index.html` to GitHub Pages.
3. Open the **hosted** app in your browser.
4. Use **Restore backup (JSON)** to import your local records.
5. Check the **History** and average cards to verify the transfer.

The local file and the hosted website use different browser storage; measurements do not transfer on their own.

## 8. Use it on your iPhone

After the GitHub Pages version is published, open it in **Safari**. To make it easier to launch, choose **Share → Add to Home Screen**. Use the same browser/site consistently for your records, and keep JSON backups.

## Privacy and care

The app stores entries in the browser on the device being used. It does not send measurements to GitHub. The website may be publicly viewable, even when it is not linked on the Ardea Apps index. Exported backup files are not encrypted, so keep them in a safe place.

**Note:** Net pad weight is an approximate measurement and can include moisture other than urine. The app helps track trends; it does not replace advice from your surgical team.
