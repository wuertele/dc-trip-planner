# Washington DC Trip Planner

A single-page destination ranker for Barbara and Laura's one-day Washington DC
trip on Thursday, May 27, 2027.

Open `index.html` locally, or publish the repository with GitHub Pages from the
repository root.

Ranks are saved in the browser with `localStorage` under
`dc-trip-rankings-v1` and synced to Supabase when the shared backend is
available. The data is keyed by stable destination IDs and person IDs, so adding
new destinations does not reset existing Barbara or Laura ranks.

Shared result links encode the selected ranks in the URL fragment. Opening a
shared link reconstructs the ranked list and saves those ranks in that browser.

The White House is intentionally excluded.

The Supabase table and row-level security policies are documented in
`supabase-setup.sql`. The browser app uses the project's publishable key only;
database passwords, access tokens, and service-role keys must not be committed.
