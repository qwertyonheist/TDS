# SMS · VAT · TDS Calculator

A lightweight, single-file calculator for SMS billing; handles VAT (13%) and TDS deductions with a clean, mobile-friendly UI. Built for internal use, deployable as a static page with zero dependencies.

## Live on

> `https://qwertyonheist.github.io/TDS/`

## Features

- **Quick Convert** - type credits to see the NPR amount, or type an amount to see credits. Both fields update each other live.
- **Credits → Amount** - enter credits and rate to calculate exactly what a client needs to pay after TDS.
- **Amount → Credits** - enter what a client actually paid (post-TDS) to back-calculate how many SMS credits they receive.
- TDS categories: Goods (1.5%), Services (5%), Rent (10%), Commission (15%), Dividend (25%), or a custom rate.
- VAT fixed at 13% on base amount throughout.
- Full breakdown table on each calculation tab.
- Dark mode via system preference.
- Mobile-friendly with safe area insets for notched devices.

## Tax Logic

| Component | Formula |
|---|---|
| Base amount | `credits × rate` |
| VAT | `base × 13%` |
| Total incl. VAT | `base + VAT` |
| TDS | `base × TDS%` |
| Client pays | `total incl. VAT − TDS` |

For reverse (Amount → Credits): `base = paid ÷ (1.13 − TDS%)`

## Built With

- Vanilla HTML, CSS, JavaScript, no frameworks
- [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) — UI font
- [Noto Sans Mono](https://fonts.google.com/specimen/Noto+Sans+Mono) — number display font

## License

MIT — use it freely.
