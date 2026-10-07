# DheseTrophies Merch — Railway Ready

This is a Railway-ready Node/Express version of the DheseTrophies merch storefront.

## Project structure

```text
dhesetrophies-merch/
├── index.html
├── style.css
├── script.js
├── server.js
├── package.json
├── railway.json
├── .gitignore
├── .env.example
└── README.md
```

## Deploy with GitHub + Railway

1. Create a new GitHub repository, for example:
   `dhesetrophies-merch`
2. Upload all files in this folder to the repository.
3. In Railway, choose **New Project** → **Deploy from GitHub Repo**.
4. Select the repository.
5. Railway will detect `package.json` and use Railpack.
6. The start command is already configured as:
   `npm start`
7. Railway provides the `PORT` environment variable automatically.
8. After deployment, open the generated Railway domain.

## Railway settings

The included `railway.json` sets:

- Builder: `RAILPACK`
- Start command: `npm start`
- Health check: `/health`
- Health check timeout: 30 seconds
- Restart policy: restart on failure, up to 10 retries

You normally do NOT need to add a custom PORT variable.

## Test locally

Install Node.js 20+ and run:

```bash
npm install
npm start
```

Then open:

```text
http://localhost:3000
```

Health check:

```text
http://localhost:3000/health
```

## Important before selling real merchandise

The current checkout is intentionally a demo. Before taking payments, connect a real commerce/payment provider such as Stripe Checkout, Shopify, Fourthwall, or a print-on-demand provider.

Also replace:
- sample product artwork
- placeholder social links
- shipping/returns text
- any placeholder branding

Make sure you have permission to use the DheseTrophies name, logos, likeness, and merchandise designs.
