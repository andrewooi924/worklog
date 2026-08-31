# Worklog

A responsive, local-first work-hours tracker. Open `index.html` in a browser, or serve the folder from any static host and add it to your phone’s home screen.

Data is stored in the browser’s `localStorage` on that device. The app supports weekly hours, quick time selection with native phone time pickers, company labels, full/half-day leave, public holidays, dark/light mode, and all-time history.

## Shared public holidays

Run [supabase-holidays.sql](supabase-holidays.sql) in the Supabase SQL editor to create the shared, read-only `public_holidays` calendar and seed the Malaysia-wide/federal 2026 holidays. These automatically count as eight hours for every user. A user can select **Adjust** on a holiday to create a personal override, or remove that override to restore the shared calendar.

The supplied dates exclude state-only holidays because the app does not yet collect a user's state. Add future or state-specific holidays only through the Supabase SQL editor; regular users have read-only access.

For local development, any static server works, for example:

```sh
python3 -m http.server 8080
```
