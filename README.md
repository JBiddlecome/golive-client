# GoLive Client Portal

## Resolving "No module named 'psycopg2'" errors

The Reports app requires the PostgreSQL driver. If you see `Data load failed: No module named 'psycopg2'` while running the Reports app:

1. Install the Python dependency:
   ```bash
   pip install -r requirements.txt
   ```
2. Ensure the environment variables for your PostgreSQL connection are set (for example `DATABASE_URL` or the individual `PGHOST`, `PGUSER`, `PGPASSWORD`, `PGPORT`, and `PGDATABASE`).
3. Restart the app after installing the dependency so the new package is picked up.

The dependency list lives in [`requirements.txt`](requirements.txt) and currently pins the binary PostgreSQL client library for portability.
