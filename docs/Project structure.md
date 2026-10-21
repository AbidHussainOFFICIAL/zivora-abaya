# Project structure

The code lives in a private repository. This is a map of how it's organised.

```
zivora-abaya
├── public/                   images, icons, web manifest, push-notification service worker
├── src/
│   ├── app/                  routes (Next.js App Router)
│   │   ├── page.tsx          homepage
│   │   ├── category/         category pages and the all-categories page
│   │   ├── product/          gallery, info tabs, reviews, size guide, sticky buy bar, recommendations
│   │   ├── search/           search page, filter bar and drawer, product cards
│   │   ├── sale/             sale page
│   │   ├── cart/             cart drawer, free-shipping progress, discount section
│   │   ├── checkout/         checkout form, order summary, shipping method, order success, WhatsApp handoff
│   │   ├── profile/          account: orders, order details, history, wishlist
│   │   ├── track-order/      order tracking
│   │   ├── auth/             sign in, register, verify, forgot and reset password, admin login
│   │   ├── admin/            admin panel
│   │   │                     products, variants, categories, orders, customers, discounts,
│   │   │                     hero, banners, reviews, size charts, statements, team
│   │   ├── api/              server routes: image upload and delete, push notifications, newsletter
│   │   ├── policies/         privacy, refund, shipping, terms
│   │   ├── about/, contact-us/, customer-service/
│   │   └── layout.tsx, manifest.ts, robots.ts, sitemap.ts, error.tsx, not-found.tsx
│   ├── components/           shared UI: header, hero, banners, best sellers, footer, product grid,
│   │                         wishlist button, support widget, floating WhatsApp, shadcn/ui parts
│   ├── providers/            React context: cart, wishlist, products, discounts, hero, banners,
│   │                         user, recently viewed
│   ├── store/                Zustand stores: cart, wishlist, products, variants, hero, banners, UI
│   ├── services/             Firestore data access, one file per area: cart, orders, products,
│   │                         variants, categories, coupons, promotions, reviews, size charts,
│   │                         announcements, wishlist, auth, notifications
│   ├── lib/                  Firebase setup, Cloudinary, pricing, formatting, Meta Pixel,
│   │                         WhatsApp links, Firestore converters
│   ├── hooks/                cart sync, checkout, coupons, free-shipping threshold, media queries
│   ├── schemas/  types/  utils/
│   └── data.ts, types.ts
├── components.json           shadcn/ui config
├── next.config.ts, tsconfig.json, eslint.config.mjs, postcss.config.mjs
└── package.json
```

Image folders under `public/` (hero slides, banners, category and about images) are left out to keep the map short.
