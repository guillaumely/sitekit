# SiteKit

Turn a short description of a local business into a fast, mobile-first, one-page website.

Most small tradespeople (plumbers, roofers, masons, hairdressers) have either no website or a free-builder page that is slow, hard to read on a phone, and hides the one thing a visitor wants: how to call them. SiteKit takes a small JSON file describing the business and generates a single static HTML page built around that.

## What a generated site has

- The phone number and a call button visible on the first screen, and a call bar that stays at the bottom on phones.
- The services, written as the problems customers actually have ("leaking pipe", "no hot water"), each with a pre-filled SMS.
- Real reviews and real project photos when the business has them, and nothing invented when it doesn't.
- A quote form that opens a pre-filled email or SMS, so there is no backend to host.
- One HTML file, no framework, no build step, no tracking.

## Status

Early. The first sites were written by hand; this repository turns the patterns they share into a generator.

Planned, in order:

1. `business.json` schema (name, trade, area, contact, services, reviews, photos, palette)
2. Generator: `node sitekit.mjs examples/plumber.json` writes `dist/index.html`
3. Three layouts that look different from each other, so two businesses in the same town never get the same site
4. Accessibility and performance checks on the output (contrast, tap targets, page weight)

## Example

`examples/plumber.json` describes a fictional business. All example data in this repository is invented; real businesses' details never go in here.

## License

MIT
