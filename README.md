# AURELIA — Premium Dubai Restaurant Website

A luxury, fully bilingual (English / Arabic) fine-dining restaurant website,
built as a portfolio demonstration to win restaurant website clients in Dubai.
Single self-contained file: **`index.html`** (~100 KB, no build step).

## Demo brand

**AURELIA — Fine Dining, Downtown Dubai** (أوريليا). A fictional demo brand.
Address, reviews, offers and menu are clearly marked **Sample** on the page —
replace them with the client's real details before use.

## What's inside

- **Cinematic hero** — full-screen photography, gold serif headline
  ("Where Taste Meets Elegance" / "حيث يلتقي المذاق بالفخامة"), scroll indicator
- **Full EN/AR switcher** — instant, no reload; Arabic flips the whole site to
  RTL (Amiri headings + Tajawal body), language persists via localStorage.
  Default language: **English**.
- **Sticky header** — transparent over the hero, dark on scroll; mobile hamburger
- **Our Story** — editorial split layout with stats
- **Signature Menu** — 24 dishes in 8 categories (Signature, Starters, Mains,
  Grilled, Seafood, Desserts, Beverages, Chef's Specials), AED prices,
  category filters, live search, bestseller + sample badges
- **Order system** — "Add to Order" builds a basket; drawer with quantities,
  totals and an **Order via WhatsApp** button (prefilled message)
- **Chef's Specials** — tasting menu, gold-leaf kunafa, wagyu tomahawk
- **Offers** — business lunch, family dining, weekend (all sample)
- **Experiences** — indoor, outdoor, private, family, events
- **Gallery** — 8 photos with full-screen lightbox (keyboard + arrows)
- **Reservation form** — name, phone (+971 default code), email, guests, date,
  time, requests; validates required fields and shows a confirmation with a
  WhatsApp send option. A request is **not** a confirmed booking until the
  restaurant approves it (stated on the page).
- **Testimonials** — sample reviews, clearly labelled, replaceable
- **Location** — Downtown Dubai sample address, Google Maps embed, directions,
  call + WhatsApp buttons
- **Instagram** — 6-tile gallery + follow button; TikTok/Facebook links
- **Footer** — full bilingual footer, developer credit to Muhammad Younus
- **SEO** — meta, Open Graph, Restaurant JSON-LD schema, semantic headings

## Customise (one place)

Everything editable lives in the **`CONFIG`** object at the bottom of
`index.html`: brand name, phone, WhatsApp, address, hours, socials, the 8
menu categories, all 24 dishes (photo, EN/AR name, EN/AR description, AED
price, bestseller flag), offers, experiences, gallery, testimonials and the
Instagram tiles. Static page text lives in the **`I18N`** dictionary (EN + AR)
right below it — every visible string, so nothing is ever half-translated.

⚠ **Contact numbers are the owner's demo number** (+92 345 7305226 — the same
number used on the Saudi restaurant template). Replace `phoneDisplay`,
`phoneLink` and `whatsapp` in CONFIG with the restaurant's own UAE number
before client use. Social handles (`@aurelia.dubai`) are samples too.

## Deploy

No build step. Any of these works:

- **GitHub Pages** — upload `index.html` to a repo, enable Pages
- **Vercel / Netlify** — drag the folder in, or `vercel --prod`
- **Any static host** — the file is self-contained (images + fonts load from
  Unsplash / Google Fonts CDNs; an internet connection is needed for photos)

## Verification (2026-11-07)

- **46/46 Playwright checks green** (test: `/tmp/dubai-test/test.py`): EN
  default + AR toggle, RTL, language persistence across reload, 8 filters,
  search (incl. no-match state), order basket (add → drawer → qty+ → AED
  totals → WhatsApp link), reservation validation + success, lightbox open/
  close/keyboard, mobile nav, **no horizontal overflow at 375/390/768/1280/
  1920 px in both languages**, zero JS/console errors.
- **All 52 photo URLs curl-verified HTTP 200**; every menu photo was viewed
  and matched to its dish (8 mismatches found during review and fixed).
- One real bug found and fixed in testing: the story stats row overflowed by
  5 px at 375 px — now wraps cleanly.
- Screenshots (EN + AR, desktop + mobile) in `screenshots/`.

## Files

- `index.html` — the whole website
- `README.md` — this file
- `screenshots/` — 7 rendered screenshots
