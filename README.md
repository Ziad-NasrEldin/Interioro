# Interioro

<img src="frontend/public/unnamed.png" alt="A quiet living room with a deep teal wall — the kind of space Interioro is built around" width="100%" />

A bilingual shop for wall decorations, wallpapers, and wall art — ready pieces on the floor, and a studio when the room needs something made.

Interioro is for people furnishing a home or a project in Saudi Arabia, and for the team that runs the catalog, orders, and design briefs behind the storefront.

- Browse products, categories, and curated bundles in Arabic or English
- Search and filter with stock you can actually see (in stock, low stock, out of stock, pre-order)
- Sign in to use the cart, save addresses, apply promo codes, and check out with location-based shipping and tax — cash on delivery or Paymob
- Ask the studio for a custom piece, a special commission from the portfolio, or a design consultation
- Run the shop from one admin desk: catalog, inventory, orders, analytics, and the request queue

## Try it

Copy `.env.example` to `.env`, fill in the database, JWT, Cloudinary, and Paymob values, then:

```bash
docker compose up -d --build
```

Open the storefront at `http://127.0.0.1:9721` (or whichever `FRONTEND_PORT` you set). Compose keeps the app on localhost; production sits behind Nginx with HTTPS.

The VPS, Nginx, and certificate runbook is in [DEPLOYMENT.md](DEPLOYMENT.md).

To work on the app without Compose: run Postgres, then `npm install` and `npm run dev` in `backend/` (migrate with `npm run db:migrate`), and the same install/dev pair in `frontend/` with `NEXT_PUBLIC_API_URL` pointing at the API origin — the Next.js route handlers already append `/api/v1`.

---

[MaVoid](https://mavoid.com) · [LinkedIn](https://linkedin.com/in/ziad-ahmed-634202332) · [GitHub](https://github.com/Ziad-NasrEldin)
