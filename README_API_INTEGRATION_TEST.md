# MASA Wallet × MASA-API — Create Wallet Integration Test

## Start MASA-API
From the MASA-API project:

```powershell
uvicorn app.main:app --host 127.0.0.1 --port 8001
```

## Run the browser test
Serve this wallet folder from a local HTTP server (recommended, instead of `file://`).

For example:

```powershell
python -m http.server 5503
```

Then open:

```text
http://127.0.0.1:5503/api_create_wallet_test.html
```

Click **Create Wallet**.

Expected:
- HTTP 200
- `success: true`
- `network: "testnet"`
- `wallet.public_key` present
- `wallet.address` present
- no `private_key`

If the browser reports a CORS error, that is the next integration item to fix in MASA-API; do not weaken wallet security or expose private keys.
