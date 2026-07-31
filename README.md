# PKO Bank Polski Executive Demo

Interactive story deck — **Pozyskanie (Acquisition) · Retencja (Retention)**.

**Live demo:** [https://zkorczyc.github.io/pko-demo/](https://zkorczyc.github.io/pko-demo/)

Navigate with **← →**, **space**, or **click**. Jump to a slide with **`#7`** (1-based).

---

## Preview locally

```bash
cd pko
python3 -m http.server 8080
# Open http://localhost:8080/demo-unified/
```

The deck must be served from the `pko/` root (not `pko/demo-unified/` alone) — slide 13 embeds the real approval e-mail from `../email-templates/examples/approval-marek.html` via `<iframe>`.

## Two acts

| Act | Persona | Card | Tagline |
|---|---|---|---|
| **01 Pozyskanie** | Michał Kowalski | PKO Mastercard Platinum | Zdobądź właściwego klienta |
| **02 Retencja** | Zofia Wiśniewska | Przejrzysta karta kredytowa | Odzyskaj z trafnością |

**Practitioner:** Karolina Nowak (both acts)

## Design notes

- **Language:** Polish throughout.
- **Colors:** PKO blue (`#0053A6`) and dark navy (`#0B2545`) as the primary palette, PKO red (`#C10016`) as the accent. Zofia's persona color is teal (`#0E8E6D`).
- **Logo:** real PKO Bank Polski logo (`assets/pko-logo.png`) on the cover slide.
- **Visuals:** no product screenshots exist yet, so every "screen" is a labelled `.img-ph` placeholder (dashed box) inside a simple phone or browser chrome — swap the placeholder `<div>` for a real `<img>` when screenshots are ready. **Exception:** slide 13 (the approval e-mail) embeds the actual working HTML template from `pko/email-templates/`, not a placeholder.
- **Partner collaboration:** RTCDP Collaboration partner is **Allegro** — Michał is a frequent Allegro shopper, a real PKO ecosystem tie-in.
- **App / payment:** **IKO** (PKO's mobile app), **BLIK** (instant payments).
- **"Journey"** always refers to the Adobe Journey Optimizer (AJO) concept and is left untranslated in the Polish copy, to avoid clashing with genuine travel content (ubezpieczenie podróżne, etc.).
- A referral act (member-get-member via **PKO Polecam**) is planned as a future addition — not built yet.

## Repository layout

| Path | Purpose |
|---|---|
| `index.html` | Self-contained interactive deck (31 slides) |
| `assets/pko-logo.png` | Real PKO Bank Polski logo |
| `adobe-wordmark-red.svg` | Footer wordmark |

## Deploy (GitHub Pages)

This repo **is** the site — `index.html` at the root, no build step. Pushed to [zkorczyc/pko-demo](https://github.com/zkorczyc/pko-demo), Pages served from `main` → `/ (root)`.

## Maintenance notes

- Replace `.img-ph` placeholders with real screenshots by swapping the inner `<div class="img-ph">…</div>` for an `<img>` — the surrounding `.phone-frame` / `.browser` chrome needs no changes.
- The slide counter (`#tot`) is computed automatically from the number of `.slide` sections in JS — no manual edits needed if you add or remove slides.
