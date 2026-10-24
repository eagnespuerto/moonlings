# 🌙 Moonlings

[![license](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![made with](https://img.shields.io/badge/made%20with-HTML5-E34F26?logo=html5&logoColor=white)](https://github.com/eagnespuerto/moonlings)
[![website](https://img.shields.io/badge/website-live-brightgreen)](https://eagnespuerto.github.io/moonlings/)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-support%20me-FF5E5B?logo=kofi&logoColor=white)](https://ko-fi.com/eagnespuerto)
[![Linktree](https://img.shields.io/badge/Linktree-soitsagnes-43E55E?logo=linktree&logoColor=white)](https://linktr.ee/soitsagnes)

*Raise a family of moons around your planet. Feed them, grow them, collect them all.*

**▶ [Play it here](https://eagnespuerto.github.io/moonlings/)**

A cozy, idle-friendly, gently physics-flavoured single-page game.
Tamagotchi × Kerbal × Universe Sandbox — but huggable.

> ### 🎨 Custom assets are still in progress
>
> Every planet, moon, ring and effect you see right now is a **placeholder SVG
> generated in code** so the game is playable and testable at this early stage.
> None of the final hand-drawn art exists yet.
>
> The full checklist of what needs drawing — **91 assets** across 4 planet types,
> 4 moon types × 5 growth stages, traits, rings, debris, effects and UI — lives in
> **[ASSETS.md](ASSETS.md)**.

---

## How to play

1. **Mine dust.** Click drifting debris in the outer field, or use the ⛏️ button.
   Dust also trickles in on its own, even while you're away.
2. **Feed** dust to a moon and it gains mass.
3. Mass carries it through five **growth stages** — it visibly gets bigger and more detailed.
4. Spend dust to **capture** new moons and grow the collection.
5. **Arrange orbits** for bonuses, and keep everyone out of the danger zone.

Everything autosaves locally. You can also export a `.moon` file and import it back.

---

## Systems

### Growth
Mass drives each moon through five stages, and both size *and* surface detail scale with it:

| Stage | Mass | |
|---|---|---|
| **Pebble** | 0 | Lumpy and irregular — not yet round |
| **Moonlet** | 6 | Just pulled itself round. First craters |
| **Moon** | 20 | Fully cratered and settled |
| **Differentiated** | 55 | Heavy stuff sank — a core glows through |
| **Atmosphere** | 110 | Wrapped in a soft halo of air and clouds |

Idle growth is slow; feeding is fast. Moons closer to the planet grow faster.

### Types
Four moon types, each with a distinct look:

- **Rocky** — dependable grey-brown, craters with lit rims.
- **Icy** — pale, crackle fissures, frost sparkles.
- **Iron** — dark, with a metallic specular sheen.
- **Volcanic** — branching lava seams that glow.

### Traits
Rolled on capture — the gotta-collect-'em hook.

- **↺ Retrograde** — orbits backwards. A little rebel.
- **👀 Tidally-locked** — always faces you. Clingy, in a nice way.
- **✦ Twinkly** — catches the light.
- **🔥 Glowing** — gives off its own warm light.

### Orbits as a gentle puzzle
Drag a moon to move it, or use the in/out buttons.

- **Closer = faster growth**, but more tidal stress.
- Cross the **Roche limit** while too massive and the moon *strains* for a few
  seconds — visibly wobbling, with a warning — before shattering into a **permanent
  ring**. The ring keeps trickling dust forever, so it's a loss, but a pretty one.
- Line two moons up at a **2:1 speed ratio** for a **harmony** dust bonus. While
  you drag, teal guide rings show exactly where a resonance would lock in, and the
  orbit gently snaps onto it.

Nothing here is punishing. The danger zone is always drawn, the break radius is
specific to each moon's mass, and you always get a warning window first.

### Saving
- Autosaves to local storage every few seconds.
- **Export** a `.moon` file (JSON) to keep or share; **import** one to restore.
- Time away is honoured on load — offline dust and offline growth, capped at 8 hours.

---

## Controls

| Input | Action |
|---|---|
| Click a moon | Select it |
| Drag a moon | Move its orbit (snaps to 2:1 resonances) |
| Click debris | Mine it for dust |
| `Space` | Mine dust |
| `C` | Capture a moon |
| `Esc` | Deselect |

---

## Running locally

It's one file with no build step and no dependencies.

```bash
git clone https://github.com/eagnespuerto/moonlings.git
```

Then open `index.html` in a browser, or serve it:

```bash
python -m http.server 8000
```

---

## Project files

| File | |
|---|---|
| `index.html` | The whole game — markup, styles, and logic |
| `ASSETS.md` | The custom-asset checklist (in progress) |
| `DESIGN.md` | The original design doc |

---

## Version

**v0.1.0** — prototype. Placeholder art.

Covers everything in the design doc's prototype scope: menu (New / Continue /
Export / Import), live orbiting SVG moons with faces, mine + feed + capture,
growth stages, types & traits, orbit push/pull with Roche shatter, harmony bonus,
autosave and file export/import.

### Stretch, not yet built
Naming ceremonies, moon moods, collision-to-merge, comet visitors, photo mode /
system portrait export, sound, achievements, procedural quirks (volcanism cycles,
ice geysers).

---

## Licence

[MIT](LICENSE)
