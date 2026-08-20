AI VIRAL WORLD — ORDER REVIEW + PRODUCT RELEASE

This version adds a manual order-review workflow:
1) Buyer pays ₹199 using the QR.
2) Buyer submits name, phone, optional email and UTR/transaction ID.
3) The server creates a pending order.
4) You open /admin and review the payment yourself.
5) You click APPROVE & RELEASE only after confirming the payment.
6) The server creates a private access token.
7) The buyer's order status changes to approved and shows the private access page.
8) The private access page contains the product URL from PRODUCT_URL.

SECURITY
- The product URL is not shown on the public landing page.
- Approval requires your server-side ADMIN_TOKEN.
- Admin token and other secrets are never placed in public/config.js.
- Do not approve an order until you independently confirm the ₹199 payment.
- This workflow is manual verification; a payment gateway webhook can be added later for automatic payment confirmation.

RUN
1) Install Node.js 18+.
2) From the project root: npm install (if using a root package manager, install server dependencies from server/).
3) cd server && npm install
4) Set environment variables:
   ADMIN_TOKEN=make-a-long-random-secret
   PRODUCT_URL=https://bit.ly/3QQ49XS
5) Start: node server.js
6) Open the public site at http://localhost:3000
7) Admin: http://localhost:3000/admin

PRODUCTION
Use HTTPS and a persistent server/volume. The included orders.json is intentionally simple; for high traffic, replace it with a managed database. Do not use a static-only host for this workflow because the order API and admin review require a server.

CUSTOMIZATION
Public content remains in public/config.js. Change price/text/productUrl/WhatsApp/features/FAQ there. PRODUCT_URL on the server is the actual released product destination.
