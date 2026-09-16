# 🌙 Moonlings — Design Doc

*Raise a family of moons around your planet. Feed them, grow them, collect them all.*

---

## Pitch
You are a young planet. Space debris drifts by. Capture it, feed it, and nurse each little moon from a pebble into a glowing, ringed, atmosphere-wrapped world with its own personality. Cozy, idle-friendly, gently physics-flavored. **Tamagotchi × Kerbal × Universe Sandbox — but huggable.**

---

## Core loop
1. **Mine dust** from the debris field (active click) — dust also trickles in passively (idle).
2. **Feed** dust to a moon → it gains mass.
3. Mass unlocks **growth stages** and new looks.
4. Spend dust to **capture** new moons and grow the collection.
5. Arrange orbits for bonuses; avoid disasters.

---

## Systems

**Feeding & growth.** Mass drives a moon through five stages:
`Pebble → Moonlet → Moon → Differentiated (core forms) → Atmosphere (gets a halo)`.
Visual size and detail scale with mass. Idle growth is slow; feeding is fast.

**Collection.** Moons come in **types** — each a distinct SVG look:
- **Rocky** — dependable grey-brown.
- **Icy** — pale, twinkles.
- **Iron** — dark, metallic sheen.
- **Volcanic** — glowing cracks.

**Traits** (rolled on capture, the "gotta-collect-em" hook):
- *Retrograde* — orbits backwards (rebel 🧡).
- *Tidally-locked* — always faces you (clingy; eyes point inward).
- *Twinkly / Glowing* — cosmetic sparkle.

**Orbital mechanics as gentle puzzle.** Pull a moon closer for faster growth, push it out for safety. Cross the **Roche limit** while too massive and it **shatters into a ring** — a loss, but a pretty one. Near-**resonant** orbits (~2:1 speed ratios) grant a small **harmony** dust bonus.

**Dangers (soft-fail, never punishing).** Roche shatter is the main risk and it's telegraphed with a visible danger zone. Nothing permadeath-y beyond it; the tone stays warm.

---

## Progression
Early: one or two moons, learning to feed. Mid: managing 4–6 moons, juggling orbits for harmony, chasing rare traits. Late: a full, humming system of differentiated worlds with atmospheres and rings — a little solar family portrait.

---

## Tone & art
Deep-space **nursery**, not hard sci-fi. Soft glows, rounded shapes, little faces with blinks. Warm amber dust against cool indigo night. All assets **hand-drawn SVG** (gradients + paths), so it stays crisp and tiny.

---

## Save system
- **Autosave** to local storage every few seconds.
- **Export** a `.moon` save file (JSON) to keep or share.
- **Import** a `.moon` file to restore.
- Idle time is honored on load (offline growth + dust).

---

## This prototype covers
Menu (New / Continue / Export / Import), live orbiting SVG moons with faces, mine + feed + capture, growth stages, types & traits, orbit push/pull with Roche shatter, harmony bonus, autosave + file export/import.

## Stretch (post-prototype)
Naming ceremonies, moon "moods," collision-to-merge, comet visitors, photo mode / system portrait export, sound, achievements, procedural moon quirks (volcanism cycles, ice geysers).
