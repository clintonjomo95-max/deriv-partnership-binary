# Deriv partnership Binary — account-based demo

This is an independent practice simulator. It is **not affiliated with or endorsed by Deriv**.

## Features
- Email and password registration/login
- Password hashing and server-side sessions
- SQLite user database and per-user virtual balance
- KSh 1,000,000 starting demo balance per account
- Simulated Forex candlesticks and demo Buy/Sell positions
- Persistent trade history for each account

## Run locally
Requires Node.js 20 or newer.

1. Extract this ZIP.
2. In the project folder, install packages:
   `npm install`
3. Set a strong session secret:
   - Linux/macOS: `export SESSION_SECRET="$(openssl rand -hex 32)"`
   - PowerShell: `$env:SESSION_SECRET = [guid]::NewGuid().ToString() + [guid]::NewGuid().ToString()`
4. Start:
   `npm start`
5. Open `http://localhost:3000`

## Deployment notes
- Deploy to a Node.js host that supports persistent disk storage.
- Set `SESSION_SECRET` to a unique, long random secret.
- Set `NODE_ENV=production` when serving over HTTPS.
- Keep the SQLite database and session database on persistent storage, and configure backups.
- Before real public use, add email verification, password reset, CSRF protection, stronger operational monitoring, privacy/terms pages, and a professional security review.
- This demo uses simulated prices and a simplified P/L model. It does not support real deposits, withdrawals, broker execution, or actual trading.
- Real-money trading/payment features may require broker authorization and regulatory/legal review in Kenya.
