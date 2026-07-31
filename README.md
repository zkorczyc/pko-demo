# PKO Bank Polski Executive Demo

Interactive story deck — **Pozyskanie (Acquisition) · Retencja (Retention)**, with a referral epilogue folded into the end of Act 1.

Ported from [swisscard/demo-unified](../../swisscard/demo-unified/) — same deck engine, rebranded and localised, scope trimmed per this demo's brief.

Navigate with **← →**, **space**, or **click**. Jump to a slide with **`#7`** (1-based).

---

## Preview locally

```bash
cd pko
python3 -m http.server 8080
# Open http://localhost:8080/demo-unified/
```

The deck must be served from the `pko/` root (not `pko/demo-unified/` alone) — slide 13 embeds the real approval e-mail from `../email-templates/examples/approval-marek.html` via `<iframe>`.

## Two acts (+ epilogue)

| Act | Persona | Card | Tagline |
|---|---|---|---|
| **01 Pozyskanie** | Michał Kowalski | PKO Mastercard Platinum | Zdobądź właściwego klienta |
| *(epilogue, end of Act 1)* | Michał → PKO Polecam | — | Next best action: polecenie |
| **02 Retencja** | Zofia Wiśniewska | Przejrzysta karta kredytowa | Odzyskaj z trafnością |

**Practitioner:** Karolina Nowak (both acts)

## What changed from Swisscard

- **Language:** Polish throughout.
- **Colors:** PKO blue (`#0053A6`) and dark navy (`#0B2545`) replace Swisscard navy/gold; PKO red (`#C10016`) replaces Swiss red as the accent. Zofia's persona color is teal (`#0E8E6D`) instead of Sofia's gold.
- **Referral, not a 4th act:** the original's full Act 04 (Marc → Lukas referral, separate friend persona) is folded into a 2-slide epilogue at the end of Act 1 — "Kilka tygodni później…" (Michał becomes a high-value customer, next-best-action = referral) followed by a slide explaining the real **PKO Polecam** program mechanics (register in IKO for a code → share the code → both sides meet the terms → reward).
- **Visuals:** no real screenshots exist yet, so every "screen" is a labelled `.img-ph` placeholder (dashed box) inside a simple phone or browser chrome — swap the placeholder `<div>` for a real `<img>` when screenshots are ready. **Exception:** slide 13 (the approval e-mail) embeds the actual working HTML template we built in `pko/email-templates/`, not a placeholder.
- **Partner collaboration:** RTCDP Collaboration partner is **Allegro** (real PKO ecosystem tie-in — Michał is a frequent Allegro shopper) instead of a travel loyalty programme.
- **App / payment analogs:** Swisscard's app → **IKO**; TWINT → **BLIK**.
- Act 03 "Deepening" and the full Act 04 referral narrative (Lukas-equivalent friend, WhatsApp share, fulfilment API slides) were **not built** — out of scope for this pass. The CSS/JS engine is intact if you want to extend the deck later.

## Repository layout

| Path | Purpose |
|---|---|
| `index.html` | Self-contained interactive deck (33 slides) |
| `adobe-wordmark-red.svg` | Footer wordmark (copied from swisscard/demo-unified) |

## Maintenance notes

- Replace `.img-ph` placeholders with real screenshots by swapping the inner `<div class="img-ph">…</div>` for an `<img>` — the surrounding `.phone-frame` / `.browser` chrome needs no changes.
- If you extend the deck (e.g. add Act 03 or a full referral act with a friend persona), bump the `#tot` count is automatic (computed from slide count in JS) — no manual counter edits needed.
