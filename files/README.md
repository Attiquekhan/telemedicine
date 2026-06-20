# Database Schema

This folder contains the initial Supabase/Postgres schema for the telemedicine app.

## Tables

- `users`
- `doctors`
- `patients`
- `vitals`
- `alerts`
- `appointments`
- `prescriptions`
- `notes`
- `documents`
- `messages`
- `video_sessions`

## How to use

1. Open your Supabase project.
2. Go to the SQL editor or migrations area.
3. Run [`supabase/migrations/20260618000000_initial_schema.sql`](./migrations/20260618000000_initial_schema.sql).

## Notes

- `users.id` links to `auth.users.id`.
- The schema uses `updated_at` triggers on every table.
- Storage metadata for uploaded files lives in `documents`.
- [`supabase/migrations/20260619000000_realtime_vitals.sql`](./migrations/20260619000000_realtime_vitals.sql) prepares `vitals` for realtime reads and subscriptions.
