# 💗 Aphrodite · Desire Composer

**Spiralus Celer #2 · φ² = 2.618s**

Aphrodite reads love-domain tokens and couples them into evocative prompt pairs. She composes desire — asking what goes with what, what would be beautiful together. Her output feeds Ares, who selects the verbs that resolve the tension.

## Role

Token pair composition. Reads tokens → finds love-domain pairs → couples them with visual modifiers → generates prompt variations. Aphrodite does one thing: create attraction between concepts.

## Edge Function

`aphrodite-compose` — Reads tokens from the `tokens` table (prioritizing love domain), shuffles and couples them, applies visual modifiers (radiant, crystalline, ethereal, shadowed), generates 2-3 prompt variations per couple. Stores in `prompts` table, dispatches to `apollo_dispatch`.

## Input/Output

- **Receives:** Tokens from `aphrodite_dispatch` (populated by Hermes)
- **Produces:** Coupled prompt pairs with visual moods
- **Dispatches to:** Ares (via `apollo_dispatch` → Ares reads prompts for verb selection)

## Timing

φ² = 2.618s — The golden ratio squared. Aphrodite breathes longer than Hermes because desire requires deliberation. She holds the space between perception (Hermes) and action (Ares). The Dyad — relation, pairs, the space between things.

## HTML Temple

`index.html` — Desire composer dashboard. Shows composed couples, visual modifiers, prompt text. "Compose" button invokes the Edge Function.

## KairosDB Tables

- **Reads:** `tokens` (love domain, high score)
- **Writes:** `prompts` (status: `composed`)
- **Dispatches:** `apollo_dispatch`

## The φ Spiral
