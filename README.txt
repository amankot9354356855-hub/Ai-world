AI VIRAL WORLD — CUSTOMER LOGIN + ORDER REVIEW VERSION

Included:
- Public sales page with product image, 2000+ videos badge, ₹199 price and QR payment.
- Customer registration/login using email + password.
- Customer passwords are hashed; passwords are never sent to WhatsApp.
- Customer account page shows their orders and approved product access.
- Admin login to review orders and approve/reject payments.
- Product access is released only after admin approval.
- Server is WhatsApp-API-ready. Normal wa.me is only a manual contact link; automatic seller notifications require WhatsApp Business/Cloud API or an approved provider.

IMPORTANT DEPLOYMENT:
1. Deploy on Node.js hosting (not GitHub Pages alone).
2. Set environment variables from .env.example. Never put secrets in public JS/HTML.
3. Change ADMIN_EMAIL, ADMIN_PASSWORD and SESSION_SECRET before going live.
4. Configure HTTPS.
5. For automatic WhatsApp notifications, configure an approved WhatsApp Business/Cloud API provider and approved message template.
6. The payment QR is manual verification. For automatic payment verification, add Razorpay/other gateway webhooks later.

CUSTOMIZATION:
- Product URL, price, WhatsApp and product title are environment variables.
- Public design/content can be edited in public/index.html.
- Product image: public/assets/product-card.png
- Payment QR: public/assets/payment-qr.jpg
