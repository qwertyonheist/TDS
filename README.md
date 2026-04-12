# SMS · VAT · TDS Calculator

A single-file offline calculator for Nepal SMS credit billing — handles VAT (13%) and TDS deductions cleanly.

## What it does

**Credits → Amount** — Enter credits and rate (excl. VAT) to get the exact amount a client needs to pay after TDS deduction.

**Amount → Credits** — Enter what a client actually paid (after TDS) to back-calculate how many SMS credits they should receive.

## Tax logic

- VAT is fixed at **13%** applied on the base rate
- TDS is deducted from the **base amount** (excl. VAT)
- Net payable = (base + VAT) − TDS

TDS categories: Goods (1.5%), Services (5%), Rent (10%), Commission (15%), Dividend (25%), or custom.

## Usage

Just open `index.html` in any browser. No install, no dependencies, works offline.

## Built with

HTML · CSS · Vanilla JS · Material Design 3 · Cambria
