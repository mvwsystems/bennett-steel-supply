# Spec Sheets

Drop spec sheet PDFs in this folder — any filename is fine, just say so and the
renaming and wiring gets handled. The names below are what the download buttons
on `/products/specifications.html` currently point at.

## Hot Rolled

| File | Profile | Status |
|---|---|---|
| `pzc.pdf` | PZC — ball and socket | **live** |
| `az.pdf` | AZ (foreign) | needed |
| `pz.pdf` | PZ — ball and socket | **live** |
| `esz.pdf` | ESZ (foreign) — Larsen interlock | **live** |
| `nz.pdf` | NZ — Larsen interlock, Blytheville AR | **live** |
| `zz.pdf` | ZZ (foreign) | needed |

## Cold Rolled

| File | Profile | Status |
|---|---|---|
| `l.pdf` | L | needed |
| `z.pdf` | Z | needed |
| `ez.pdf` | EZ | needed |
| `xz.pdf` | XZ | needed |
| `dz.pdf` | DZ — hook and grip, Iuka MS | **live** |
| `jz.pdf` | JZ | needed |

## Flat / Pan / Trench

| File | Profile | Status |
|---|---|---|
| `ps.pdf` | PS — sheet also covers PZ sections | **live** |
| `s.pdf` | S (cold rolled) | **live** |
| `kd.pdf` | KD (cold rolled) | needed |
| `sks-14.pdf` | SKS-14 (cold rolled) | **live** |

## H-Piles

No spec sheets — the owner asked for a plain list of HP 8"–14" sections, which
the page already shows.

## Notes

The branded "Cut Sheet" PDFs are extracts from a 9-page master
(`Cut Sheet Master.xlsx`) — PZC is page 5, PZ page 6, DZ page 8. The remaining
pages likely cover several of the profiles still marked *needed* above, so the
full master is worth asking for.

`esz.pdf` is the newer full ESZ table (ESZ17-630 → ESZ36-700). It replaced an
older two-row extract covering only ESZ-19/20-700.

## Adding one by hand

A row with no PDF keeps the disabled grey "Coming Soon" button. To activate it,
drop the file in and swap that row's button:

```html
<!-- from -->
<button class="btn-dl">Download PDF</button>
<!-- to -->
<a class="btn-dl" href="/assets/spec-sheets/az.pdf" download>Download PDF</a>
```

Live buttons render gold; the teal "Email It to Me" button stays either way.
