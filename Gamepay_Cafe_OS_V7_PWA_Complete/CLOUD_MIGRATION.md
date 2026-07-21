# Gamepay Cafe OS V7 Cloud Migration

V7 is a production-bridge package, not a falsely pre-connected cloud service.

## Included now
- Flask server application
- persistent SQLite database
- stronger PBKDF2 PIN hashing with legacy hash migration
- role/session enforcement
- JSON dashboard health API
- installable-PWA foundation (manifest + service worker)
- Docker/Gunicorn deployment files
- environment-variable secrets
- cloud/WhatsApp readiness status screen
- all V6 business modules

## PostgreSQL migration contract
The current application remains runnable with SQLite. For real multi-location/public-cloud deployment,
replace the sqlite3 data-access layer with PostgreSQL/SQLAlchemy or a PostgreSQL adapter, run schema
migrations, and set DATABASE_URL. Do not merely set DATABASE_URL and assume migration is complete.

## WhatsApp automation contract
Automatic sending requires an approved WhatsApp Business setup, customer consent where required,
approved templates where required, credentials, and webhook/message-status handling. V7 exposes
configuration placeholders but does not fabricate successful sending.

## Production security checklist
- HTTPS only
- strong GAMEPAY_SECRET
- rotate bootstrap PINs
- CSRF protection
- rate limiting/login lockouts
- encrypted backups
- least-privilege database credentials
- immutable off-site audit backup
- monitoring and restore drills
