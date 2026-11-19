# WeGolden Syria Arabic landing page (draft)

Internal draft only. Not published, not uploaded, and not pushed to any remote.

This folder is a git-ready copy of the Arabic RTL landing page intended for `https://wegolden-mena.com/ar/syria/` once anh Tùng approves the go-live in his own words.

## Files

- `index.html` — page with logo, favicon and mascot also embedded as data URIs; the landing video is a separate file under `assets/`
- `wegolden-logo.png` — official WeGolden wordmark
- `wegolden-mena-mascot.png` — official WeGolden MENA mascot (Telegram `@wegoldenmena` avatar)
- `wegolden-favicon.png` — official favicon
- `assets/wg-syria-video.mp4` — 30s Arabic landing video (H.264/AAC, 1280×720, +faststart), re-encoded from Drive `content` / `Second Version` / `WeGolden-30s-Glass-16x9-AR.mp4`
- `assets/wg-syria-video-poster.jpg` — poster frame from the same video

The working copy also lives at `/workspace/wg-syria/landing-syria-ar.html`. A pre-edit backup is at `/workspace/wg-syria/landing-syria-ar.v2-before.bak.html`.

## How to set the WhatsApp number

Edit **one** JavaScript constant near the bottom of `index.html`:

```js
const WHATSAPP_NUMBER = 'PLACEHOLDER_NUMBER';
```

Replace it with the business number in international format, digits only, no `+` or spaces. Example:

```js
const WHATSAPP_NUMBER = '9715XXXXXXXX';
```

The prefilled Arabic message is in `WHATSAPP_TEXT` in the same script. Every WhatsApp button (floating button, contact section, hero, footer) reads this constant.

Note: WhatsApp Business may not reach Syrian numbers using `+963`. Keep the Telegram button (`https://t.me/wegoldenmena`) as the fallback.

## Before go-live

Confirmed: open-account CTAs point to `https://my.wegolden.com`. The minimum deposit for Syrian clients is 10 USD via USDT. Other payment methods remain unlisted pending confirmation.

1. Remove `<meta name="robots" content="noindex, nofollow">`.
2. Confirm the page is actually served at `https://wegolden-mena.com/ar/syria/` (this path is not live today; it currently 404s after a redirect to `/syria/`).
3. Have a native Arabic speaker review the copy.
4. Replace `PLACEHOLDER_NUMBER` as above.

## TODO-VERIFY

These items are also marked as HTML comments (`TODO-VERIFY`) in `index.html` and are **not** stated as facts in visible copy:

- Remove `noindex,nofollow` when the page is approved and live at the canonical URL.
- `https://wegolden-mena.com/ar/syria/` is not live yet (404 after redirect to `/syria/`).
- Legal and licence links use the live root URLs `https://wegolden-mena.com/legal-compliance/` and `https://wegolden-mena.com/licenses/` (the `/ar/…` equivalents redirect here). Confirm Arabic-path versions if a locale subdirectory is launched.
- Full 20% tradeable bonus T&Cs (cap, minimum deposit, withdrawal, expiry) are not in the knowledge base, so they are not stated on the page. “Terms apply” currently links to the public legal-compliance page; confirm if a dedicated bonus T&C URL should be used instead.
- Formal Swap-Free T&C (S-07) may still differ from the 11 November 2026 announcement (deposit tiers, 5-day gold holding rule). The page follows the 11/11 announcement and states that company terms apply.
- Numeric spread values after the 11/11 update are not in the source set, so they are not listed.
- Payment, deposit and withdrawal methods for Syria other than USDT deposit still need per-method confirmation; only USDT deposit (minimum 10 USD for Syrian clients) is listed.
- Syria Facebook (`https://www.facebook.com/WeGoldenSyria`) and Instagram (`https://www.instagram.com/wegolden_syria/`) are live. The Telegram channel is still the MENA channel: `https://t.me/wegoldenmena`.
- Set `WHATSAPP_NUMBER` when the business number is connected. WhatsApp Business may not reach `+963`; keep Telegram as the fallback.
- No segregated-funds / client-money wording was found in `/workspace/datahub/wegolden-mena/` or the learning channel, so it is omitted from trust badges.
- Arabic copy still needs a native-speaker review.
- Google Ads may still not allow CFD/forex ads targeting Syria.
- FinCEN MSB is a money-services registration, not a trading licence, and is omitted from the licence block.
- Open Graph image currently uses the live official logo URL (crawlers cannot read a data-URI). Upload a dedicated share image if required.

## Off-page SEO (cannot be done from this HTML file)

After the page is live on the canonical URL: add it to the sitemap, submit it in Search Console, set internal links and hreflang on the rest of wegolden-mena.com, and measure page speed on the real host.
