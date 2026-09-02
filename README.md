# NICE SHIRT — show page

Static one-page site for **NICE SHIRT**, The Second City Grad Revue
(Chicago e.t.c. Theater, Aug–Sept 2026). Hosted on GitHub Pages at
**https://niceshirt.rizzo.cc/** and linked from the theater credits on rizzo.cc.

## What's on the page

- Performance list with a separate ticket link per date. Past dates are
  crossed off automatically (a show counts as done 3 hours after curtain),
  and the next upcoming show is highlighted. Previews and opening night are
  listed for the record.
- Cast grid with headshots, plus the creative team.
- The other Grad Revue ensemble on the bill, WAITING FOR THE PUNCHLINE.
- About: the show blurb, the Grad Revue 3 description, and the sketch /
  improv / stand-up definitions.
- Venue: address, parking, seating, accessibility, age policy, drinks, and
  the "bring a jacket" note.
- Structured data (schema.org TheaterEvent) for each upcoming ticketed show.

## Editing

Everything lives in `index.html`. The performance list is the `SHOWS` array
near the bottom of the file: one line per show with start time (Chicago
time), label, price, and ticket URL. Cast names and headshot filenames are
in the `CAST` array; headshots live in `assets/cast/`.

Optional venue photo: drop a photo of the e.t.c. room in `assets/` and set
`VENUE_PHOTO` (next to the `SHOWS` array) to its path, e.g.
`'assets/etc-stage.jpg'`. While it is empty the Venue section shows no photo.

Analytics: shared rizzo.cc GA4 property. Turn it off on one device with
`?ga=off` (and back on with `?ga=on`).

## Hosting

GitHub Pages from `main`, custom domain via `CNAME`. DNS is a CNAME record
`niceshirt` → `yada-yoda.github.io` (DNS only, not proxied) on the rizzo.cc
zone at Cloudflare.

## Changelog

### v0.1.0 — 2026-09-02
First release. Built so the cast has one link to share for tickets instead
of three separate checkout URLs, and so the show has a home once the run is
over. Includes the full performance history (previews and opening night
crossed off), the cast, the second ensemble on the bill, and the practical
venue details audiences keep asking about.
