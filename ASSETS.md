# 🎨 Moonlings — Asset List

Everything the game currently draws with **placeholder SVG generated in code**
(`index.html`, see `buildMoonArt()`, `buildPlanet()`, `drawRings()`).
This is the checklist of hand-drawn assets to replace them with.

> **Status: custom assets not started.** The shapes below exist only as
> procedural placeholders so v0.1.0 is playable and testable.

---

## Conventions

| Thing | Convention |
|---|---|
| Format | Hand-drawn **SVG** — gradients + paths only, no rasters |
| Moon art | Authored in a **unit circle** (`r = 1`, origin at centre), scaled at runtime |
| Planet art | Authored at **`r = 54`** in an 800×800 scene |
| Naming | `moon-<type>-<stage>.svg`, `planet-<type>-<part>.svg`, `fx-<name>.svg` |
| Palette | Warm amber dust (`#ffd99b → #ff8f4d`) against cool indigo night (`#0b0a1f → #1e1b4d`) |
| Line feel | Soft, rounded, `stroke-linecap:round`; nursery, not hard sci-fi |
| Faces | Separate layer — they rotate independently of the body |
| Budget | Keep each file small; these all live inline in a single HTML page |

---

## 1. Planets — 4 types × 3 pieces = 12

The player picks one at **New planet**. Each needs a base sphere, a surface
treatment, and an outer glow.

| Type | Palette | Surface treatment (placeholder → wanted) |
|---|---|---|
| **Violet** | `#8f7bff → #5b47c9 → #2c2270` | banded swirls → soft aurora bands, drifting |
| **Ember** | `#ffb27a → #d4553a → #5e1c24` | lava stripes → cracked crust with glowing seams |
| **Frost** | `#dff4ff → #79b6d8 → #2c4d78` | polar caps → ice caps + frozen sea texture |
| **Verdant** | `#a8f0b8 → #48ad7c → #1c4a48` | blob continents → continents, shallows, cloud wisps |

- [ ] `planet-violet-base.svg` · `planet-violet-surface.svg` · `planet-violet-halo.svg`
- [ ] `planet-ember-base.svg` · `planet-ember-surface.svg` · `planet-ember-halo.svg`
- [ ] `planet-frost-base.svg` · `planet-frost-surface.svg` · `planet-frost-halo.svg`
- [ ] `planet-verdant-base.svg` · `planet-verdant-surface.svg` · `planet-verdant-halo.svg`

### Shared planet face set — 6
Recoloured per planet via its `ink` colour.

- [ ] `planet-face-eyes-open.svg`
- [ ] `planet-face-eyes-blink.svg` (blink frame)
- [ ] `planet-face-eye-highlight.svg`
- [ ] `planet-face-mouth-happy.svg`
- [ ] `planet-face-mouth-worried.svg` (a moon is straining)
- [ ] `planet-face-blush.svg`

**Subtotal: 18**

---

## 2. Moons — 4 types × 5 stages = 20 bodies

The heart of the list. Size **and detail** both grow with mass.

| Stage | Mass | What it should read as |
|---|---|---|
| **Pebble** | 0 | Lumpy, irregular, not yet round. Tiny. |
| **Moonlet** | 6 | Just pulled itself round. First craters. |
| **Moon** | 20 | Fully cratered, settled, characterful. |
| **Differentiated** | 55 | Heavy stuff sank — a core glows through. |
| **Atmosphere** | 110 | Wrapped in a soft halo of air + clouds. |

### Rocky — *dependable grey-brown* (`#c9b8a4 → #6d5b48`)
- [ ] `moon-rocky-pebble.svg` · [ ] `moon-rocky-moonlet.svg` · [ ] `moon-rocky-moon.svg`
- [ ] `moon-rocky-differentiated.svg` · [ ] `moon-rocky-atmosphere.svg`
- Craters with a light rim and dark floor; dusty, matte, friendly.

### Icy — *pale, twinkles* (`#eaf6ff → #7fb8e6`)
- [ ] `moon-icy-pebble.svg` · [ ] `moon-icy-moonlet.svg` · [ ] `moon-icy-moon.svg`
- [ ] `moon-icy-differentiated.svg` · [ ] `moon-icy-atmosphere.svg`
- Crackle fissures across the surface, frost sparkles, translucent edges.

### Iron — *dark, metallic sheen* (`#cfd3da → #4a4d5a`)
- [ ] `moon-iron-pebble.svg` · [ ] `moon-iron-moonlet.svg` · [ ] `moon-iron-moon.svg`
- [ ] `moon-iron-differentiated.svg` · [ ] `moon-iron-atmosphere.svg`
- One strong specular sweep, subtle banding, a dark impact pit.

### Volcanic — *glowing cracks* (`#ffcaa0 → #5a1f14`)
- [ ] `moon-volcanic-pebble.svg` · [ ] `moon-volcanic-moonlet.svg` · [ ] `moon-volcanic-moon.svg`
- [ ] `moon-volcanic-differentiated.svg` · [ ] `moon-volcanic-atmosphere.svg`
- Branching lava seams, each with a hot core stroke and a soft bloom behind it.

### Per-type extras — 8
- [ ] `moon-core-rocky.svg` · `moon-core-icy.svg` · `moon-core-iron.svg` · `moon-core-volcanic.svg`
      *(the glowing interior revealed at Differentiated)*
- [ ] `moon-atmo-rocky.svg` · `moon-atmo-icy.svg` · `moon-atmo-iron.svg` · `moon-atmo-volcanic.svg`
      *(the atmosphere shell + cloud arcs)*

### Shared moon face set — 6
Scaled to the moon; rotates to face outward, or inward when tidally-locked.

- [ ] `moon-face-eyes-open.svg` · [ ] `moon-face-eyes-blink.svg`
- [ ] `moon-face-eye-highlight.svg`
- [ ] `moon-face-mouth-happy.svg` · [ ] `moon-face-mouth-worried.svg` *(straining)*
- [ ] `moon-shadow-terminator.svg` *(shared sphere shading overlay)*

**Subtotal: 34**

---

## 3. Trait overlays — 7

Rolled on capture. These sit on top of any type/stage combination.

- [ ] `trait-retrograde.svg` — a small backwards-arrow badge on the orbit path
- [ ] `trait-tidal.svg` — a subtle "looking at you" eye-line cue
- [ ] `trait-twinkly-sparkles.svg` — 3–4 frame sparkle sheet
- [ ] `trait-glow-rocky.svg` · `trait-glow-icy.svg` · `trait-glow-iron.svg` · `trait-glow-volcanic.svg`
      *(warm aura, tinted per type)*

**Subtotal: 7**

---

## 4. Rings — 5

What a moon becomes when it crosses the Roche line. It should read as a *pretty
loss*, not a failure state.

- [ ] `ring-rocky.svg` · [ ] `ring-icy.svg` · [ ] `ring-iron.svg` · [ ] `ring-volcanic.svg`
- [ ] `ring-particle-texture.svg` — the fine grain that fills a ring band

**Subtotal: 5**

---

## 5. Debris field & dust — 6

The thing you actually mine.

- [ ] `debris-chunk-a.svg` · [ ] `debris-chunk-b.svg` · [ ] `debris-chunk-c.svg` · [ ] `debris-chunk-d.svg`
- [ ] `dust-mote.svg` — the single amber grain
- [ ] `dust-puff-sheet.svg` — the burst when debris is mined

**Subtotal: 6**

---

## 6. Effects — 5

- [ ] `fx-shatter-burst.svg` — the moment a moon lets go
- [ ] `fx-feed-sparkle.svg` — dust landing on a moon
- [ ] `fx-capture-flash.svg` — a new moon arriving
- [ ] `fx-harmony-arc.svg` — the teal link between two resonant moons
- [ ] `fx-strain-cracks.svg` — overlay while a moon is straining

**Subtotal: 5**

---

## 7. UI — 12

- [ ] `icon-dust.svg` · [ ] `icon-harmony.svg`
- [ ] `icon-mine.svg` · [ ] `icon-feed.svg` · [ ] `icon-capture.svg`
- [ ] `icon-orbit-in.svg` · [ ] `icon-orbit-out.svg`
- [ ] `icon-menu.svg`
- [ ] `logo-wordmark.svg` — "Moonlings" for the menu
- [ ] `favicon.svg` — currently an inline placeholder
- [ ] `ui-roche-line.svg` — the dashed danger boundary treatment
- [ ] `og-card.svg` — social/share card

**Subtotal: 12**

---

## 8. Background — 4

- [ ] `bg-starfield-near.svg` · [ ] `bg-starfield-far.svg`
- [ ] `bg-nebula-warm.svg` · [ ] `bg-nebula-cool.svg`

**Subtotal: 4**

---

## Totals

| Group | Count |
|---|---:|
| Planets (4 types + shared face) | 18 |
| Moons (4 types × 5 stages + extras) | 34 |
| Trait overlays | 7 |
| Rings | 5 |
| Debris & dust | 6 |
| Effects | 5 |
| UI | 12 |
| Background | 4 |
| **Total** | **91** |

---

## Suggested order

1. **Moon bodies for one type, all 5 stages** (Rocky) — proves the growth read end to end.
2. **The shared moon face set** — it is most of the charm, and it is reused everywhere.
3. **The other three moon types** — this is where the collection hook lives.
4. **Planets** — 4 types, seen constantly but only one at a time.
5. **Rings + shatter FX** — the emotional beat.
6. **Debris, dust, traits** — texture on the core loop.
7. **UI, background, share card** — polish.

---

## Stretch assets (post-prototype)

Matching the design doc's stretch list:

- [ ] Moon **mood** faces (sleepy, delighted, grumpy)
- [ ] **Comet visitor** sprite + tail
- [ ] **Merge** animation for collision-to-merge
- [ ] Naming-ceremony frame / certificate
- [ ] Photo-mode **system portrait** border
- [ ] Achievement badges
- [ ] Ice-geyser and volcanism-cycle animation frames
