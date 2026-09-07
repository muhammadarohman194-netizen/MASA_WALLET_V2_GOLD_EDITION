# MASA Wallet V2 — Gold Edition

A polished MASA Wallet prototype based on the agreed dark + gold visual direction and the official MASA coin artwork supplied for the project.

## Included
- Premium MASA Wallet home
- MASA balance + fiat display
- Assets: MASA + MSR
- Send / Receive flows
- QR Scan + My QR flow shell
- Activity history
- Security / Connected Apps settings shell
- Trade button/card -> separate MASA DEX project
- Miner button/card -> separate MASA Miner project

## Separate-project navigation
The Wallet intentionally acts as the gateway. It does **not** merge DEX or Miner code into the Wallet.

Default routes:
- MASA DEX: `http://127.0.0.1:5500`
- MASA Miner: `http://127.0.0.1:8080`

Change them in `js/app.js` under `MASA_APPS` if the ports change.

## Run
Serve this folder with any static HTTP server. Example:

```bash
python -m http.server 8080
```

Then open `http://127.0.0.1:8080`.

> Demo note: balances and transaction rows are UI demo data. Sending/receiving is not connected to MASA CORE yet.
