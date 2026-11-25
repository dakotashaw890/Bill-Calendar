# Bill Calendar — version 1.0

A local-first, installable Progressive Web App (PWA) for bills and paydays. No server account, bank connection, ads or external libraries. No personal records are included in this website folder.

## Host for free on GitHub Pages
1. Extract the ZIP. Create a GitHub repository named `bill-calendar`. A public repository is suitable for these generic app files; **do not upload My-Bills-Private.json or any exported backup**.
2. Upload the extracted files themselves (index.html, app.js, style.css, manifest.webmanifest, sw.js, icon PNGs, README.md) to the repository root, not a nested directory. Commit to `main`.
3. Under repository Settings → Pages, select Deploy from a branch, then `main` and `/ (root)`, and save. Open the published HTTPS URL shown on the Pages screen. Typically `https://YOUR-USERNAME.github.io/bill-calendar/`.
4. Open that URL in Chrome on Android. Use Install app if offered, or Chrome menu → Add to Home screen / Install app. On iPhone, open the URL in Safari and choose Share → Add to Home Screen.
5. On your phone, download the separate **My-Bills-Private.json** file, open the installed app, then Settings → Import bill file and select it. Confirm import. Your data stays in local browser storage, not on GitHub.
6. Add payday schedules and enter today's available checking balance under Settings. No balances or income estimates are invented.

## Use
- Calendar: tap a date; tap a bill name to edit its individual amount or completion status; checkmark completes just that occurrence. Future months repeat automatically.
- Bills: add, edit or delete schedules; supports weekly, biweekly, monthly, quarterly, annual and one-time recurrence. Short months clamp to the last day.
- Summary: scheduled bills, income, category totals, and an illustrative 30-day balance projection using today's entered available balance. It excludes past due amounts and unscheduled spending, and is not a bank balance. A fresh balance entry is required each day. On a single day, bills are applied before income (conservative assumption). Mark items already reflected in the entered balance completed to avoid double-counting.
- Settings: export regular JSON backups; import replaces existing data after confirmation. Install and offline access require a first successful HTTPS visit (or localhost for testing). Browser data removal can erase records. No encryption beyond the device/browser security; protect your device and keep backups private.

## Private seed data notes
The separate bill import file is based on previously identified recurring transactions, not a fresh account sync or verified due dates. It contains 26 estimated regular charges and one annual vehicle registration item. Dates earlier than Nov 25, 2026 were advanced to their next monthly occurrence rather than marked paid or overdue without verification. Future dates can be edited. Monthly recurrence is assumed for regular charges, including water; verify the water billing frequency, the Fifth Third payment identity and all amounts. No additional timeshare debt is added, to avoid potentially duplicating Fifth Third. No historical payments are marked complete. Actual posting dates can differ from estimates.

## Limitations
No background push notifications, live bank syncing, or automatic cross-device sync. The app flags overdue bills inside the calendar. Do not rely on it as the sole source of payment due dates. Browser storage is specific to the web origin and device. Source is plain HTML/CSS/JS; no build step needed.
