# Prompts for Claude

## New site from the brief
Read BRIEF.md. Replace every {{PLACEHOLDER}} in every file with the brief's values. Create one page per specialty under services/ by copying services/anxiety-therapy/index.html, renaming the folder to the slug, and rewriting the content for that specialty and city. Update the nav links on every page, the services list on index.html, sitemap.xml, and the schema block on every page. Write page titles like "Anxiety Therapy in Salt Lake City | Jane Smith, LCSW". Keep sentences short and plain. Don't change the design or CSS.

## Edit request from a client
In the {{CLIENT}} repo, on the {{PAGE}} page, {{CHANGE}}. If the page's topic changes, update its title and meta description too. Keep everything else untouched.

## New specialty page
Copy services/anxiety-therapy/index.html to services/{{SLUG}}/index.html. Rewrite it for {{SPECIALTY}} in {{CITY}}: h1, title, description, intro, "who this is for" list, "what we'll work on", and the FAQ. Add it to the nav on every page, the services list on the home page, and sitemap.xml.

## Retheme
In css/style.css, change the :root colors to {{PALETTE}} and the fonts to {{FONTS}}. Keep contrast readable. Change nothing else.
