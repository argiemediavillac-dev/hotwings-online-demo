# Hotwings Online (demo)

Public preview: https://argiemediavillac-dev.github.io/hotwings-online-demo/

A browser-only ordering prototype for **Hotwings, Rosal St., Poblacion, Polomolok**. It runs as one static page (`index.html`). The "server" is simulated inside the page and enforces prices, stock, order steps and role permissions. Data stays in the visitor's browser. No order reaches the restaurant, no money moves, and no SMS is sent.

## What's in it

- **Customer:** the full menu (80 items) with the 6 wing flavors, a cart, delivery or pickup checkout with a map pin and demo barangay fees, cash on delivery or pickup, manual GCash reference checking, a live order tracker with a demo rider map, receipts, and help and policies. Trays, packages and packed meals are pre-order only (date at least 24 h ahead; packed meals minimum 12).
- **Kitchen and Manager:** order board, accept, prepare, ready and reject, prep-time override, menu availability and stock counts, GCash verification, cash collection, rider dispatch, reports with CSV, store settings and delivery zones.
- **Admin:**
  - **Analytics:** most requested items, flavor share, Pareto, menu engineering, recipe costing with ideal price at a target food cost, price ladders and package value, ingredient inventory cover and reorder points, and a 12-month income projection with scenarios.
  - **Photos:** upload, edit (zoom, move, rotate, fit, background), replace, delete and restore the logo and every product photo.
  - Audit log.
- **Rider:** offers with masked customer details, trip steps, simulated GPS sharing (including denied and stale states) and PIN proof of delivery.
- **Demo guide:** 6 guided scenarios and 27 automated acceptance checks.

## Sources and assumptions

- Menu and prices: Hotwings Facebook menu post, **20 Jan 2024**. Confirm current prices with the store.
- Logo: supplied by the owner (`img/logo.webp`, `icon-*.png`).
- Wing photos: cropped from the owner's promo images in `assets/source/`. The crops leave out the old price text.
- `assets/source/menu.png` is an older owner menu with different prices (8 pcs ₱160, 24 pcs ₱450, milk tea, ice cream). The app uses the Facebook menu. Confirm which one is current.
- Ingredient costs, stock counts, fixed costs, delivery zones and fees, and the 30-day sales history in Analytics are **assumptions or simulated** and are labeled in the app. Opening hours and GCash merchant details aren't published yet.

## Before real operation

GitHub Pages only serves static files. Real orders, shared photos, cross-device GPS, accounts and reports need an authenticated backend (for example Supabase Postgres with row-level security, Realtime and Storage) and server-side checks on price, fee, stock, payment and role. Do not put service keys in these files.
