# TEAM VILLAIN — Generation Prompt Packs

These are **prompts, not assets.** Each pack holds copy-pasteable `<prompt>` strings for an
image, video or audio bot. Generating them is a separate act — some are done, most are not.

All packs inherit from `00-brand-bible.xml`. Read that file once before generating anything;
its `<casting>` block in particular is the thing people get wrong.

---

## Status at a glance

**24 of 44 assets exist.** The website is complete — every slot on the page is filled. The six
social teasers are also built now, sitting outside the site in `social/`. What remains unbuilt
is everything else the *site doesn't consume*: extra hero alternates, b-roll, emblem
treatments, and the extra audio cues.

| | Built | Prompt only |
|---|---|---|
| Website assets | **18** | 0 |
| Social teasers | **6** | 0 |
| Extra b-roll / film / merch | 0 | **20** |

If you never generate another one, the site is finished and you have six teasers ready to
post. The remaining 20 are raw material for brand films, invitations and merch — useful when
you get there, not before.

---

## BUILT

| Asset ID | Type | Aspect | Where it appears |
|---|---|---|---|
| `VLN-VID-01` | video | 16:9 | Hero background loop — empty ballroom, haze through a gold doorway |
| `VLN-VID-02` | video | 16:9 | The Time Machine background — server hardware, gold bokeh |
| `VLN-IMG-01` | still | 3:4 | Ch. I The Verdict — figure in a doorway |
| `VLN-IMG-02` | still | 4:5 | Ch. II The Label — cracked gold mask |
| `VLN-IMG-03` | still | 4:5 | Ch. II The Broken Heart — kintsugi vessel |
| `VLN-IMG-04` | still | 4:5 | Ch. II The Turn — black tie, mask lowered |
| `VLN-IMG-05` | still | 21:8 | Gatherings — The Masquerade banner |
| `VLN-IMG-06` | still | 16:10 | Gatherings — The Midnight Table |
| `VLN-IMG-07` | still | 16:10 | Gatherings — Velocity |
| `VLN-IMG-08` | still | 16:10 | Gatherings — Passport |
| `VLN-IMG-09` | still | 16:10 | Gatherings — The Vault |
| `VLN-IMG-10` | still | 16:10 | Gatherings — Ibiza |
| `VLN-IMG-11` | still | 16:10 | Gatherings — Miami penthouse |
| `VLN-IMG-12` | still | 16:10 | Gatherings — The Charter |
| `VLN-IMG-13` | still | 21:8 | Gatherings — South Africa banner |
| `VLN-FDR-01` | still | 3:4 | The Founder — **a real photograph**, graded, not generated |
| `VLN-FDR-02` | still | 3:4 | Founder alternate — shadow band across the eye line |
| `VLN-AUD-01` | audio | — | Site ambience — 56s seamless loop, 68 BPM, C minor, opt-in toggle |

`VLN-FDR-01/02` have **no prompt pack and never will.** They are Andre's own photograph, cut
out and graded into the palette. A specific real person's face is never generated — if the
founder imagery changes, it changes by taking another photograph.

`VLN-AUD-01` was **synthesised from scratch**, not prompted — see `05-audio-mood.xml`
`<delivered>` for the full arrangement. It is owned outright with nothing to license.

| Asset ID | Type | Aspect | Where it appears |
|---|---|---|---|
| `VLN-SOC-01` | video | 9:16 | Social — "They Chose Sides" (ballroom doorway) |
| `VLN-SOC-02` | video | 9:16 | Social — "The Receipt" (cracked gold mask macro) |
| `VLN-SOC-03` | video | 9:16 | Social — "Hours For Money" (dormant machinery abstraction) |
| `VLN-SOC-04` | video | 9:16 | Social — "You Can't Come Back" (penthouse glass) |
| `VLN-SOC-05` | video | 9:16 | Social — "The Room You Weren't In" (dining table) |
| `VLN-SOC-06` | video | 9:16 | Social — "Six In The Morning" (empty racetrack) |

The six social teasers live in **`social/`**, not `assets/` — they were built for Reels and
TikTok and **never touch the website**, so they sit outside the media-slot system entirely.
Post them with the hook lines and captions already written into `06-social-teasers.xml`.

---

## NOT BUILT — prompts ready, nothing generated

Nothing below is on the site and nothing below is missing from it.

**Hero alternates** — `01-hero-motion.xml`
`VLN-VID-01-ALT-A` (rain on black glass, 16:9 10s) · `VLN-VID-01-ALT-B` (gold in smoke,
16:9 12s) · `VLN-VID-01-V` (vertical hero crop, 9:16 10s). Only worth generating if you
tire of the ballroom, or want a mobile-specific hero.

**B-roll** — `02-broll-motion.xml`
`VLN-VID-03` cars on a wet street · `VLN-VID-04` penthouse skyline · `VLN-VID-05` jet stairs
at dawn · `VLN-VID-06` the midnight table · `VLN-VID-07` masks in close · `VLN-VID-08` yacht
and dark coastline · `VLN-VID-09` racetrack at sunrise · `VLN-VID-10` villa pool at night.
These are for **edited films**, not the site — the page uses stills for these scenes because
fifteen video loops would make it unusable on a phone.

**Emblem treatments** — `04-emblem-motifs.xml`
`VLN-EMB-01` black marble backplate · `VLN-EMB-02` gold foil emboss · `VLN-EMB-03` wax seal ·
`VLN-EMB-04` animated logo reveal (16:9 4s) · `VLN-EMB-05` favicon/avatar plate ·
`VLN-EMB-06` invitation card. For invitations, decks, merch and video intros. Every one is a
**backplate to sit the existing mark on** — the emblem itself is never regenerated.

**Additional audio** — `05-audio-mood.xml`
`VLN-AUD-02` trailer cue · `VLN-AUD-03` tension/engine cue · `VLN-AUD-04` stinger library.
For films and cutdowns. The site only needs `VLN-AUD-01`, which exists.

---

## How to generate one

Open the pack, find the `<asset>` block by `id`, paste the whole `<prompt>` into your bot.
The strings are complete — style suffix, lighting doctrine and palette hexes are already
baked in, so nothing needs assembling. Paste `<negative_prompt>` into the negative field; in
Midjourney convert it to `--no term, term`. Read `<notes>` **before** burning credits: it
names the specific failure mode for that shot and tells you when to bin a take rather than
fight it.

For video, generate a still first and drive image-to-video where the tool supports it —
Runway and Kling both hold the look far better from an approved start frame than from text.

**Casting is not optional.** Every prompt with a person in it already states that the subject
is Black, and carries the skin-lighting correction: key about a stop hotter than the room,
fill the shadow side, let the sheen roll rather than clip. Unprompted generators default to
white subjects, and the house lighting recipe will swallow deep skin tones into unreadable
silhouette if you strip that clause out. Don't.

## How to install one

Save it next to `index.html` as `assets/<ASSET-ID>.jpg` for stills or `.mp4` for motion —
e.g. `assets/VLN-VID-04.mp4`. Nothing else. The page's media loader reads `data-asset` on
each slot and probes `.jpg` `.png` `.webp` then `.mp4` `.webm`; the first file that loads
replaces the placeholder. There is no manifest to edit.

Note that a slot has to *exist on the page* for a file to appear. Dropping in `VLN-VID-05`
does nothing on its own — the site has no jet-stairs slot. Those assets are for films.

**Export settings.** Stills: 1900px on the long edge (2200 for 21:8 banners), sRGB, JPEG 82.
The whole current media set is 5.8 MB, and that's the budget worth protecting. Video: H.264
MP4, `yuv420p`, faststart, 24fps, **no audio track**, under 2 MB per loop.
