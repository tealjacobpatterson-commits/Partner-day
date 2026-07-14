# Teal Products Partners Day 2026

Static site for the Teal Products Partners Day 2026 event — RSVP form, confirmation
ticket, and itinerary. No build step or server required; it's plain HTML/CSS/JS.

## Pages

| File | Purpose |
|------|---------|
| `index.html` | RSVP form (entry point) |
| `confirmation.html` | "Thank you" page — attendee ticket, Add to Calendar, LinkedIn share |
| `itinerary.html` | Event itinerary (web page) |
| `itinerary-graphic.html` | Source for the shareable itinerary graphic |
| `itinerary-graphic.png` | Exported itinerary graphic (also used as the confirmation page's social preview image) |
| `assets/` | Logos and brand graphics |

## Flow

`index.html` → on submit, redirects to `confirmation.html` with the attendee's
details in the URL. The confirmation page draws a personalised ticket on a `<canvas>`
and offers "Add to Calendar" (`.ics` download) and a LinkedIn share preview.

> **Note:** the RSVP form does not yet send submissions anywhere — it only passes the
> details to the confirmation page. Wire it to your email/CRM/Klaviyo before going live.

## Deploy with GitHub Pages

1. Push this folder to a GitHub repository.
2. Repo **Settings → Pages** → Source: **Deploy from a branch** → `main` / root.
3. Your site will be live at `https://<user>.github.io/<repo>/`.

## Editing key details

- **Event date/time/venue** — search the HTML files for `17 September 2026`,
  `9:30 AM`, and `Alexandra Way`.
- **Calendar times** — in `confirmation.html`, the `.ics`/calendar block uses UTC
  (`20260917T083000Z`–`20260917T150000Z` = 09:30–16:00 BST).
- **`[product name]`** placeholder appears in `index.html` and `itinerary.html`.
