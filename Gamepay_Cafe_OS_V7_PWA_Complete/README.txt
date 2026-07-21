GAMEPAY CAFE OS V7 — PRODUCTION BRIDGE BUILD

V7 ADDS
- Installable PWA foundation (manifest/service worker)
- Stronger PBKDF2 PIN hashing with automatic legacy-hash migration
- Health/dashboard JSON API endpoints
- Docker + Gunicorn deployment configuration
- Environment-based secrets/configuration
- Cloud/WhatsApp readiness dashboard
- Production migration documentation
- All V6 features retained

LOCAL RUN
1. Install Python 3
2. Extract ZIP
3. Double-click start_windows.bat
4. Open http://127.0.0.1:5000

DOCKER RUN
docker compose up --build

IMPORTANT
V7 is cloud-ready architecture, but this ZIP is NOT automatically connected to a real cloud database
or WhatsApp account. Real cloud sync requires deployed infrastructure and PostgreSQL migration.
Real automatic WhatsApp messages require approved provider credentials/configuration.
