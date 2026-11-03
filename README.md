# Apartment 3D

A browser planner for a 10.35 × 10.05 m apartment, furnished with IKEA Malaysia pieces. Orbit the plan, jump between rooms, click an item for its price and product page, then swap, move, or add furniture. The shopping list updates as you edit and can be exported as CSV. Edits stay in this browser.

Furniture models and prices belong to IKEA. This is a personal plan, not an IKEA product.

## Run locally

```bash
python3 -m http.server 8080
```

Open http://127.0.0.1:8080. On localhost every model is read from this folder. Three.js loads from unpkg, so the first visit needs a network connection.

Drag to orbit, scroll to zoom. `Swap / edit` turns on move, rotate, swap, and delete.

## Repo

| Path | What it is |
|---|---|
| `index.html` | The viewer |
| `models/` | Models placed in the original plan |
| `library/` | Swap catalog: product data, thumbnails, and models |

Two pieces have no IKEA model (POÄNG rocking chair, GULDVÄVARE mobile) and are drawn as simple stand-ins.

## Deploy

Vercel’s Hobby plan accepts about 100 MB per upload. Production hosts the furnished plan and the picker thumbnails. Extra swap models load from this public repo through jsDelivr. Localhost is unchanged.
