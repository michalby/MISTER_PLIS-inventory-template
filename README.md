# The lab's inventory

An empty inventory for MISTER PLIS: the lab's reagents and consumables (tips, membranes, vials…), where they are and
what to order — kept as two Excel workbooks in git, so every change is recorded with who made it.

## Start

1. On GitHub, **Use this template → Create a new repository**. Make it **private**: the inventory is the lab's own.
2. Give your MISTER PLIS server a token for it that may **write** (a fine-grained token: this repository only,
   *Contents: Read and write*), on Settings → Server & updates → GitHub access. The server sends each change here.
3. On the server: the setup page (or Settings → Reagents & consumables) → this repository's address → **Sync**. Then,
   **Start an empty inventory** (on the same Settings tab): the server makes the empty workbooks here (`reagents.xlsx` and
   `consumables.xlsx`) and you can add the first items.

## What is here

| File | What it is |
|---|---|
| `reagents.xlsx` | one row per reagent (sheet `reagents`); the `columns` sheet says what each column means |
| `reagents.csv` | the same rows as text, rewritten with every change (easy to read in a diff) |
| `consumables.xlsx`, `consumables.csv` | the same for consumables |
| `mister_plis.json` | how the reagents are shown on the server (file names, list columns, quick filters) |
| `info/` | notes people leave from the lab (e.g. “bottle almost empty”), for correcting the records later |

You can open the workbooks in Excel and change them there too: the server merges both sides cell by cell when it
syncs, and stops only when the same cell was changed differently in both places.
