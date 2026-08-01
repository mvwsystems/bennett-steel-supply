# Spec Sheets

Drop spec sheet PDFs in this folder. Filenames must match exactly — the download
buttons on `/products/specifications.html` are wired to these paths.

All lowercase, `.pdf` extension, no spaces.

## Hot Rolled

| File | Profile | Status |
|---|---|---|
| `pzc.pdf` | PZC | needed |
| `az.pdf` | AZ (foreign) | needed |
| `pz-ps.pdf` | PZ — shared with PS below | **live** |
| `esz.pdf` | ESZ (foreign) | **live** |
| `zz.pdf` | ZZ (foreign) | needed |

## Cold Rolled

| File | Profile | Status |
|---|---|---|
| `l.pdf` | L | needed |
| `z.pdf` | Z | needed |
| `ez.pdf` | EZ | needed |
| `xz.pdf` | XZ | needed |
| `dz.pdf` | DZ | needed |
| `jz.pdf` | JZ | needed |

## Flat / Pan / Trench

| File | Profile | Status |
|---|---|---|
| `pz-ps.pdf` | PS — same file as PZ above | **live** |
| `s.pdf` | S (cold rolled) | **live** |
| `kd.pdf` | KD (cold rolled) | needed |

## Unfiled

- `sks-14.pdf` — present but not linked from any row. SKS-14 isn't one of the
  section names on the specs page; confirm which row it belongs to (or whether
  SKS-14 should be its own row) before wiring it.

## H-Piles

No spec sheets — the owner asked for a plain list of HP 8"–14" sections, which
the page already shows.

## Adding one

A row with no PDF keeps the disabled grey "Coming Soon" button. To activate it,
drop the file in with the name above and swap that row's button:

```html
<!-- from -->
<button class="btn-dl">Download PDF</button>
<!-- to -->
<a class="btn-dl" href="/assets/spec-sheets/az.pdf" download>Download PDF</a>
```

Live buttons render gold; the teal "Email It to Me" button stays either way.
