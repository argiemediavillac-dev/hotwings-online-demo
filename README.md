# HOTWINGS ONLINE demo

Public preview: https://argiemediavillac-dev.github.io/hotwings-online-demo/

This is a browser-local prototype. Menu prices were transcribed from screenshots supplied by the owner; current availability and prices need store confirmation. No order reaches the restaurant, no payment is charged, and no SMS is sent automatically.

## Available in the preview

- Delivery and pickup checkout with itemized totals, demo zone fees, cash and manual GCash reference states.
- Optional customer map pin using browser GPS, requested only after the customer taps the location button.
- Store order board, manual payment verification, item availability, and rider workflow in the same browser.
- Optional foreground rider GPS for an assigned job, displayed only in this browser with timestamp and accuracy. Sharing stops when the rider turns it off or leaves the rider role.
- SMS compose links for staff to review and send an order update from a phone's messaging app.
- Customer order history, receipts, reorder, store sales totals, product quantities and best sellers. Completed orders are used for sales rankings; collected payments are not inferred.
- Separate profile and product photo controls. The profile photo can be copied to a product. Photos are resized and stored in the browser.

## Needed before real operation

GitHub Pages only serves static files. Real customer-to-store orders, cross-device GPS, shared photos, secure accounts, order history, and staff reports need an authenticated backend and database with server-side price, fee, inventory, payment, and role checks. Configure verified delivery zones and fees. Manual GCash needs verified public merchant details and an independent payment verification process. Automated SMS needs an approved SMS provider, consent, and server-side credentials. Do not put service secrets in these files.

The deployed static files are in `dist/`. Open `dist/index.html` or serve `dist/` with a static HTTP server. Use the role switcher to explore customer, store, and rider flows.
