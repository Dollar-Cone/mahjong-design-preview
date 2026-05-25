# Mahjong Studio — public website design preview

Static HTML mockups for the public-side redesign of
[The Mahjong Studio](https://github.com/Dollar-Cone/Mahjong) website
(issue [#1183](https://github.com/Dollar-Cone/Mahjong/issues/1183)).

**🔗 Live: <https://dollar-cone.github.io/mahjong-design-preview/>**

## What this is

A self-contained set of static HTML pages for product-owner review.
It is **not** the real Next.js app; nothing here is wired to data,
booking, payments, or auth. Pages exist to evaluate copy, layout,
typography, palette, photo treatment, and information architecture.

The design is anchored to two product-owner-owned source-of-truth
documents in the main repo:

- `docs/product/mahjong-public-customer-funnel-functional-spec.docx`
  — guest-first public customer funnel
- `docs/product/the-mahjong-studio-canva-asset-production-brief.docx`
  — Pam's approved brand kit (Playfair Display + Montserrat + cream /
  blush / dusty blue / charcoal / gold)

## What's in here

| Page | Purpose |
| --- | --- |
| `index.html` | Cover sheet linking the seven pages with one-line notes |
| `home.html` | Landing page with hero, "right now" strip, decision block |
| `classes.html` | Learn page with how-it-works steps, month calendar, and class list |
| `sessions.html` | Open play page with filter chips, month calendar, and session list |
| `membership.html` | Two-tier membership with FAQs |
| `help.html` | Question-keyed help organized by what visitors actually ask |
| `contact.html` | Lead with email/phone/address; short contact form |
| `about.html` | Studio backstory + four-step "your first visit" walkthrough |

## How to give feedback

Look at copy, palette, photo treatment, and IA. The pages are
deliberately static; links inside often go to `#` because nothing is
wired up. Useful kinds of feedback:

- "I'd say this differently" — copy reactions
- "I want to see X first" / "X is buried" — layout reactions
- "This isn't on-brand" / "This looks great" — visual reactions
- "I would never use this" / "I'd use this every time" — task fit

Less useful right now (we know):

- Mobile burger menu isn't built
- Buttons hover but don't navigate
- Placeholder names (Sandra, Marian) need real attribution
- Dates and pricing are illustrative

## Running locally

The folder is fully static. Open any `.html` file in a browser, or:

```
python -m http.server 5173 --bind 0.0.0.0
```

Or via Docker:

```
docker run -d --rm -p 5173:80 \
  -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Then visit <http://localhost:5173/index.html>.

## Cache busting

`_shared.css` is served with a `?v=N` query string from every page.
Bump that number when you change the CSS so reviewers don't see
stale styles from browser cache.

---

Built for product-owner review by Jeff (jeff.leblanc@dollarconenc.com).
Disposable — delete when the design is settled in the main app.
