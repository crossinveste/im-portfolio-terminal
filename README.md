# Investment Management — Live Portfolio & Attribution Frame

Live Link: **https://crossinveste.github.io/im-portfolio-terminal/**

## Security & Live Sync Architecture
1. **Passkey-Encrypted Access (`PBKDF2-HMAC-SHA256`):** All portfolio data (`index.html` seed and `data/snapshot.json`) is cryptographically encrypted at rest before being stored in this repository. Entering the team passkey decrypts the live dashboard strictly in-memory inside the viewer's browser.
2. **Real-Time Auto-Sync:** Unlocked sessions poll GitHub every 10 seconds via conditional HTTP `ETag` requests and automatically decrypt & refresh on screen whenever a new Feeder Excel snapshot is published.
3. **Zero Dollar `MV` / `AUM` Exposure:** Raw `.xlsx` workbooks are parsed and stripped of all dollar `MV` and `AUM` values locally in the uploader's browser before encryption and upload.
