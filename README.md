# Bin Day PWA

A mobile-first installable PWA for tracking household bin collections.

## Features
- Add multiple bin collection schedules.
- Collection day: Monday to Friday.
- Bin types: General waste (green), Recycling (blue), Garden waste (black).
- Weekly or fortnightly collection frequency.
- Select the next collection date; it must match the selected weekday.
- Calculates upcoming dates and shows the next collection at the top.
- Edit or delete saved schedules.
- Offline app shell and local storage.
- Requests browser notification permission and checks for an 8pm reminder the evening before collection.

## Important notification limitation
This is a static PWA, so it does **not** have a push-notification server. Browsers do not reliably run scheduled JavaScript while a PWA is fully closed. Reminders are checked while the app is open, and when it is reopened or brought back into view. To guarantee a native notification at 8pm while the app is closed, add a push backend/service (for example, a scheduled server job plus Web Push) or package as a native app with local notification scheduling.

## Deploy to GitHub Pages
1. Create a GitHub repository and upload all files/folders in this directory.
2. In repository **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
3. Open the published HTTPS URL on your phone.
4. Use your browser's **Add to Home Screen / Install app** option.
5. Open the app and tap the notification status line to request permission.

Collection information is saved in the browser's local storage on that device. It does not sync between devices.
