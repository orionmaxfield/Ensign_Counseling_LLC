# Therapist Practice Site — Master Template

Hand-coded static site for a small therapy practice. No build step. Copy it, fill in the brief, push to GitHub, host on Cloudflare Pages.

## How to use for a new client

1. Click **Use this template** on GitHub and name the new repo after the client.
2. Fill in `BRIEF.md` with the client's details.
3. Give Claude this prompt (also in `PROMPTS.md`):
   > "Read BRIEF.md. Replace every `{{PLACEHOLDER}}` across all files with the brief's values. Create one page per specialty under `services/` by copying `services/anxiety-therapy/index.html`. Update the nav on every page, `sitemap.xml`, and the schema block on every page. Don't change the design."
4. Add the client's photo as `images/clinician.jpg` (under 300 KB, WebP preferred).
5. Push. Connect the repo to Cloudflare Pages (preset: None, output dir: `/`).
6. Run the launch checklist in `CHECKLIST.md`.

## Placeholders

Every `{{NAME}}` must be replaced before launch. Search the repo for `{{` to find stragglers.

| Placeholder | Example |
| --- | --- |
| `{{PRACTICE_NAME}}` | Jane Smith Counseling |
| `{{CLINICIAN_NAME}}` | Jane Smith |
| `{{CREDENTIALS}}` | LCSW |
| `{{CITY}}` | Salt Lake City |
| `{{STATE}}` | UT |
| `{{STATE_FULL}}` | Utah |
| `{{STREET}}` | 123 Main St, Suite 200 |
| `{{ZIP}}` | 84101 |
| `{{PHONE_DISPLAY}}` | (801) 555-0100 |
| `{{PHONE_TEL}}` | +18015550100 |
| `{{EMAIL}}` | hello@example.com |
| `{{DOMAIN}}` | https://www.janesmithcounseling.com (no trailing slash) |
| `{{SPECIALTY_1}}` / `{{SPECIALTY_1_SLUG}}` | Anxiety Therapy / anxiety-therapy |
| `{{FORMSPREE_ENDPOINT}}` | https://formspree.io/f/abcdefgh |
| `{{HOURS_SCHEMA}}` | Mo-Fr 09:00-17:00 |
| `{{HOURS_DISPLAY}}` | Monday–Friday, 9 am–5 pm |
| `{{LAT}}` / `{{LNG}}` | 40.7608 / -111.8910 |

## Structure

```
index.html                  Home
about/index.html            About the clinician
services/<slug>/index.html  One page per specialty (copy the example)
fees/index.html             Fees and insurance
contact/index.html          Contact form + map link
404.html                    Not-found page
css/style.css               All styles; colors in :root at the top
js/main.js                  Mobile nav only
sitemap.xml  robots.txt     SEO
_redirects                  Cloudflare redirects (for WordPress migrations)
```

## SEO already built in

- Unique `<title>` and `<meta name="description">` slot on every page
- One `<h1>` per page, written the way clients search
- Canonical link on every page
- LocalBusiness + Person schema (JSON-LD) on every page
- Clean folder URLs (`/services/anxiety-therapy/`)
- Open Graph tags for link previews
- `sitemap.xml`, `robots.txt`
- Mobile-first, no external scripts, fast by default

## Retheming per client

Change the six colors and two fonts at the top of `css/style.css`. Nothing else needs to move.

## Content placeholders (Claude writes these from the brief)

`{{WHO_PLAIN}}`, `{{APPROACH_SENTENCE}}`, `{{APPROACH_PARAGRAPH}}`, `{{CREDENTIALS_LONG}}`, `{{SPECIALTY_2}}`/`{{SPECIALTY_3}}` (+ `_SLUG`, `_LOWER`, `_BLURB`, `_LEAD`, `_INTRO`), `{{SYMPTOM_1..4}}`, `{{WHAT_WE_WORK_ON}}`, `{{SESSION_DESCRIPTION}}`, `{{FAQ_1..3}}`, `{{BIO_LEAD}}`, `{{BIO_PARAGRAPH_1..2}}`, `{{DEGREE}}`, `{{SCHOOL}}`, `{{TRAINING_1..2}}`, `{{LICENSE_NUMBER}}`, `{{CONSULT_LENGTH}}`, `{{FEES_SENTENCE}}`, `{{SESSION_FEE}}`, `{{INSURANCE_LIST}}`, `{{SLIDING_SCALE}}`, `{{CANCELLATION_POLICY}}`, `{{REPLY_TIME}}`, `{{MAP_QUERY}}` (URL-encoded address), `{{PARKING_NOTE}}`, `{{TELEHEALTH_SENTENCE}}`.

Tip: if a client only has one or two specialties, delete the extra list items on the home page rather than leaving placeholders.
