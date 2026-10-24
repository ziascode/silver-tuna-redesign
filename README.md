# Silver Tuna Restoration: site redesign

A single-page, mobile-first redesign of [silvertuna.ca](https://www.silvertuna.ca/) (painting and heritage restoration, Stratford, Ontario), built to turn visits into site-visit bookings.

## Run it

```bash
python3 -m http.server 4331
```

Then open http://localhost:4331. To view it on a phone on the same Wi-Fi, add `--bind 0.0.0.0` and open `http://<this-computer's-ip>:4331`.

## What's in it

- **Hero:** five period paint layers sweep away in WebGL to reveal a restored century porch, with a "paint core" panel naming each layer.
- **Paint-core colour bands** recur in the menu, service swatches, booking progress and the footer wordmark.
- **Sections:** a statement with inline photos, sticky-stage services (with "Book this" per trade), a before/after slider, a Stratford heritage band, the crew list and the booking section.
- **Booking:** a 4-step form (work, building, preferred day and time, contact) that opens as a bottom sheet from every call to action.

## Booking delivery

With no backend, the final step opens the visitor's messages app with the request pre-written to 226-921-5308. To receive bookings directly, set `CONFIG.endpoint` near the top of the script to a form service URL (Formspree, Jobber, etc.). The page then POSTs the request as JSON.

## Credits

All photographs are Silver Tuna's own, loaded from their Squarespace CDN. Libraries: GSAP 3.12.5, ScrollTrigger, Lenis 1.1.13. Fonts: Gloock, Instrument Sans, IBM Plex Mono (Google Fonts).
