# Landing brief

Business facts for this page. Claude reads it before writing anything and never invents what is missing.

Short, reusable values (brand, colours, URL, title, headline, CTA, form endpoint, author, verification codes)
live in `site.config.json`, not here: the build puts them into every page. This file holds everything else.

## Identity
- LOGO: (brak — favicon generowany z liter BC; prawdziwe logo do pozyskania od klienta)
- Social profiles (become schema.org `sameAs`):
  - https://www.instagram.com/BC.Clippers/
  - https://www.facebook.com/profile.php?id=61588855171556
  - https://booksy.com/pl-pl/325140_bc-clippers-barbershop_barber-shop_8820_krakow

## Hosting
- REPO_NAME: bc-clippers
- REPO_OWNER: GKunc
- CUSTOM_DOMAIN: (brak, github.io)

## Business
Źródło: profil Booksy (stan na 2026-11-18).
- Nazwa na Booksy: BC.CLIPPERS Barbershop; Instagram: BC.Clippers
- What is offered: barber shop — strzyżenie męskie, strzyżenie maszynką, broda, golenie brzytwą z gorącym ręcznikiem, tonowanie włosów i brody (farba American Crew), depilacja woskiem nos/uszy. Mycie i stylizacja włosów są w cenie każdego strzyżenia.
- Cennik (Booksy):
  - Strzyżenie męskie (Haircut) — 110 zł, 1 h
  - Strzyżenie maszynką (Clipper haircut) — 90 zł, 30 min
  - COMBO BASIC (strzyżenie + trymowanie brody) — 150 zł, 1 h 15 min
  - COMBO CLIPPERS (strzyżenie + broda z gorącym ręcznikiem) — 180 zł, 1 h 30 min
  - Tonowanie głowy (Hair coloring/camouflage) — 90 zł, 30 min
  - Strzyżenie brody (Beard Trimming) — 80 zł, 30 min
  - Broda + podgolenie z gorącym ręcznikiem — 110 zł, 45 min
  - Tonowanie brody (American Crew) — 70 zł, 30 min
  - Tonowanie + trymowanie brody — 140 zł, 50 min
  - Golenie twarzy lub głowy brzytwą (Hot towel shave) — 120 zł, 40 min
  - Depilacja woskiem nos/uszy (Waxing) — 35 zł, 10 min
  - Na Booksy dostępne też pakiety usług.
- Barberzy: Yevhen, Tatiana, Piotrek
- Target audience: mężczyźni w Krakowie (Śródmieście, okolice Rakowickiej); obsługa także po angielsku (nazwy usług dwujęzyczne)
- Location / service area: Rakowicka 22D, 31-521 Kraków (Śródmieście)
- Godziny: pon–pt 10:00–21:00, sob 9:00–21:00, niedz. zamknięte
- Rezerwacja: wyłącznie Booksy (brak formularza na stronie)
- Telefon: brak w źródle

## Proof (real only)
- Testimonials: brak zgody na cytowanie opinii z Booksy — nie cytujemy.
- Numbers / results (with source):
  - Ocena 5.0/5 na podstawie 244 opinii na Booksy (stan na 18.11.2026)
- Client logos: brak

## FAQ (real questions customers ask; becomes the FAQ section + FAQPage schema)
Odpowiedzi wyłącznie z faktów powyżej.

## Author (for blog posts and E-E-A-T; name and URL go into site.config.json)
- AUTHOR_BIO: (brak)

## Voice
- Tone: konkretny, męski, bez przesady; krótkie zdania; „Ty”
- Words to use / avoid: unikać superlatywów („najlepszy w Krakowie”) bez źródła

## SEO
- Primary keyword: barber Kraków
- Secondary keywords: barber shop Kraków Śródmieście, strzyżenie męskie Kraków, barber Rakowicka, golenie brzytwą Kraków, trymowanie brody Kraków
- Competitors / reference sites: (brak)

## Forms, analytics, compliance
- Contact form: brak — tylko przycisk do Booksy
- Who receives enquiries: n/d
- Analytics wanted: none
- AI_CRAWLERS: allow-all
- LEGAL_ENTITY: Piotr Maliszewski (dane biznesu z Booksy)
- CONTACT_EMAIL: kontakt@bcclippers.pl — PLACEHOLDER wskazany przez użytkownika; domena bcclippers.pl nie istnieje (2026-11-18). Do potwierdzenia u klienta przed przekazaniem strony.

## Facts Claude must not invent
- telefon, rok założenia, liczba klientów, doświadczenie barberów, parking, płatność kartą, cytaty z opinii

## site.config.json cheat sheet
| Key | What to put |
| --- | --- |
| BRAND, BRAND_INITIAL | name; one letter for the generated favicon |
| THEME_COLOR | brand accent as 6-digit #hex |
| LANG, LOCALE | e.g. `pl` and `pl_PL` |
| LEGAL_ENTITY, CONTACT_EMAIL | who is responsible for the site (privacy policy) |
| SITE_URL | (auto, publish skill) https URL without trailing slash |
| INDEXNOW_KEY | (auto) `openssl rand -hex 16` |
| PAGE_TITLE | 30-60 chars incl. brand, primary keyword first |
| H1_HEADLINE, SUBHEADLINE, CTA_LABEL | hero copy and button label |
| META_DESCRIPTION | 120-155 chars, with a reason to click |
| LLMS_SUMMARY | 2-4 plain sentences: what the business is, for whom, where |
| BLOG_TITLE, BLOG_DESCRIPTION | needed from the first post on |
| AUTHOR_NAME, AUTHOR_URL | blog author (LinkedIn or about page) |
| FORM_ENDPOINT | (auto with the form worker: `node tools/form-worker.mjs deploy`) or the external form service URL |
| FORM_PROVIDER | who processes the form, for the privacy policy ("Cloudflare and Resend" with the worker) |
| EMAIL_FROM | sender of the autoreply; domain verified in Resend |
| FORM_NOTIFY_TO | who gets enquiries (empty = CONTACT_EMAIL) |
| TURNSTILE_SITE_KEY | Cloudflare Turnstile site key (anti-bot check, needed for the autoreply) |
| FORM_ACCESS_KEY | only for services that need a key in the form (e.g. Web3Forms) |
| ANALYTICS, ANALYTICS_ID | `none`, `plausible` (id = domain, may stay empty), `goatcounter` (site code), `cloudflare` (token), `ga4` (G-…) |
| PRIVACY_UPDATED | YYYY-MM-DD |
| GOOGLE_SITE_VERIFICATION, BING_SITE_VERIFICATION | filled after launch (`node tools/google.mjs verification-token`) |

## Wygląd (nawiązuje do logo)
- Logo: napis CLIPPERS — białe, ciężkie sportowe wersaliki z czarną obwódką i srebrną krawędzią, na czarnym tle z dwiema ukośnymi srebrnymi liniami (zdjęcie z Booksy).
- Strona jest zawsze ciemna (czerń, biel, srebro); THEME_COLOR = czerń.
- `src/og.png` jest robiony ręcznie z `brief/og-source.html` (Chrome headless, 1200×630). `node tools/make-assets.mjs` go nadpisze: po jego uruchomieniu wygeneruj og.png ponownie z tego pliku.
