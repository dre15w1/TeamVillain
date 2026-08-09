# TEAM VILLAIN

A private-society landing experience. Dark luxury, narrative scroll, invitation-only framing.

> *"They chose sides. We chose each other."*

---

## What's in here

```
index.html          the entire website (single self-contained file)
assets/             drop your logo + generated media here
xml/                generation prompt packs for image / video / audio bots
```

The site is one file. No build step, no dependencies, no framework. Open `index.html`
in a browser or serve the folder statically and it works.

---

## 1. Swap in the real logo

The site ships with a hand-built **vector emblem** that closely matches the Team Villain
mark. It's used everywhere the logo appears (seal, nav crest, hero, footer).

To use your real artwork instead, drop the file at:

```
assets/team-villain.png
```

A transparent PNG works best (the site applies its own gold glow behind it). The swap is
automatic — if the file is missing, the vector emblem is used, so the site never breaks.

To point somewhere else, edit one line near the bottom of `index.html`:

```js
const BRAND = {
  logo: 'assets/team-villain.png',   // ← path, or a base64 data URL
  ...
};
```

---

## 2. Drop in generated media

Every image and video on the page is a **slot** with a stable asset ID. Until a file
exists, the slot renders as a styled placeholder showing its ID — so you always know
exactly what's missing and where it goes.

To fill a slot, save the generated file into `assets/` named after its ID:

| Slot | Save as | Section |
|---|---|---|
| `VLN-VID-01` | `assets/VLN-VID-01.mp4` | Hero background loop |
| `VLN-VID-02` | `assets/VLN-VID-02.mp4` | The Engine background |
| `VLN-IMG-01` | `assets/VLN-IMG-01.jpg` | The Verdict |
| `VLN-IMG-02..04` | `assets/VLN-IMG-0N.jpg` | The Mask triptych |
| `VLN-IMG-05..09` | `assets/VLN-IMG-0N.jpg` | The Gatherings |

Accepted extensions: `.jpg` / `.png` / `.webp` for stills, `.mp4` / `.webm` for motion.
Refresh and it appears. No code change needed.

The prompts that produce these files live in [`xml/`](xml/) — see
[`xml/README.md`](xml/README.md) for the full asset map.

---

## 3. Wire up the application form

"Request an Audience" currently logs to the console. Point it at a real endpoint —
Formspree, a Cloudflare Worker, a Next.js route, whatever you're using. Near the bottom
of `index.html`:

```js
document.getElementById('audienceForm').addEventListener('submit', e => {
  e.preventDefault();
  ...
  fetch('/api/audience', { method: 'POST', body: new FormData(f) });   // ← your endpoint
```

Fields submitted: `name`, `contact`, `city`, `archetype`, `build`, `give`, `vouch`, `code`.

---

## Structure of the narrative

The page is written as seven chapters, in order:

1. **The Verdict** — the origin wound. Why the group exists.
2. **The Mask** — why "villain" is worn on purpose.
3. **Doctrine** — six tenets the circle doesn't cross.
4. **The Engine** — the system that buys back time. Deliberately veiled.
5. **The Gatherings** — the Masquerade, Midnight Table, Velocity, Passport, the Vault.
6. **The Circle** — archetypes, not a roster.
7. **Request an Audience** — the gate.

---

## Notes

- Fully responsive; mobile nav collapses to a full-screen overlay.
- Respects `prefers-reduced-motion` (reveals and embers turn off).
- Fonts load from Google Fonts. To go fully offline, self-host Bodoni Moda, Cinzel and Jost
  and swap the `<link>` in `<head>`.
- No analytics, no trackers, no third-party scripts beyond the font stylesheet.

---

*By invitation. Always.*
