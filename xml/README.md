# TEAM VILLAIN — Generation Prompt Packs

XML prompt packs for image and video generation bots. Every asset entry carries a complete,
copy-pasteable `<prompt>` string, a `<negative_prompt>`, an aspect ratio, and notes.

All packs inherit from `00-brand-bible.xml`. Read that file once before generating anything.

---

## Asset map

| Asset ID | Pack file | Type | Aspect | Duration | Consumed by |
|---|---|---|---|---|---|
| VLN-VID-01 | `01-hero-motion.xml` | video | 16:9 | 8–12s | Hero section `#top` — full-bleed background behind the centered emblem |
| VLN-VID-01-ALT-A | `01-hero-motion.xml` | video | 16:9 | 10s | Hero alternate (rain on black glass) |
| VLN-VID-01-ALT-B | `01-hero-motion.xml` | video | 16:9 | 12s | Hero alternate (gold in smoke) |
| VLN-VID-01-V | `01-hero-motion.xml` | video | 9:16 | 10s | Mobile / vertical hero crop |
| VLN-VID-02 | `02-broll-motion.xml` | video | 16:9 | 10s | ENGINE section `#engine` — full-bleed background under body copy |
| VLN-VID-03 | `02-broll-motion.xml` | video | 16:9 | 8s | B-roll — exotic cars, wet street at night |
| VLN-VID-04 | `02-broll-motion.xml` | video | 16:9 | 10s | B-roll — penthouse skyline |
| VLN-VID-05 | `02-broll-motion.xml` | video | 16:9 | 8s | B-roll — private jet stairs at dawn |
| VLN-VID-06 | `02-broll-motion.xml` | video | 16:9 | 10s | B-roll — the midnight table |
| VLN-VID-07 | `02-broll-motion.xml` | video | 16:9 | 8s | B-roll — gold masks, masquerade close |
| VLN-VID-08 | `02-broll-motion.xml` | video | 16:9 | 10s | B-roll — yacht and dark coastline |
| VLN-VID-09 | `02-broll-motion.xml` | video | 16:9 | 8s | B-roll — rented racetrack at sunrise |
| VLN-VID-10 | `02-broll-motion.xml` | video | 16:9 | 12s | B-roll — villa pool at night |
| VLN-IMG-01 | `03-stills.xml` | still | 3:4 | — | THE VERDICT chapter `#verdict` |
| VLN-IMG-02 | `03-stills.xml` | still | 4:5 | — | THE MASK section `#mask` — card 1, "The Label" |
| VLN-IMG-03 | `03-stills.xml` | still | 4:5 | — | THE MASK section `#mask` — card 2, "The Broken Heart" |
| VLN-IMG-04 | `03-stills.xml` | still | 4:5 | — | THE MASK section `#mask` — card 3, "The Turn" |
| VLN-IMG-05 | `03-stills.xml` | still | 21:8 | — | GATHERINGS `#gatherings` — full-width banner, "The Masquerade" |
| VLN-IMG-06 | `03-stills.xml` | still | 16:10 | — | GATHERINGS `#gatherings` — grid card, "The Midnight Table" |
| VLN-IMG-07 | `03-stills.xml` | still | 16:10 | — | GATHERINGS `#gatherings` — grid card, "Velocity" |
| VLN-IMG-08 | `03-stills.xml` | still | 16:10 | — | GATHERINGS `#gatherings` — grid card, "Passport" |
| VLN-IMG-09 | `03-stills.xml` | still | 16:10 | — | GATHERINGS `#gatherings` — grid card, "The Vault" |
| VLN-EMB-01 | `04-emblem-motifs.xml` | still | 1:1 | — | Emblem backplate — black marble (section dividers, decks, merch) |
| VLN-EMB-02 | `04-emblem-motifs.xml` | still | 1:1 | — | Emblem backplate — gold foil emboss on bone paper |
| VLN-EMB-03 | `04-emblem-motifs.xml` | still | 1:1 | — | Wax seal backplate (site seal, envelopes, sign-offs) |
| VLN-EMB-04 | `04-emblem-motifs.xml` | video | 16:9 | 4s | Animated logo-reveal backplate (video intros, outros) |
| VLN-EMB-05 | `04-emblem-motifs.xml` | still | 1:1 | — | Favicon + social avatar backplate |
| VLN-EMB-06 | `04-emblem-motifs.xml` | still | 4:5 | — | Invitation card mockup (social, email headers, apply section) |
| VLN-AUD-01 | `05-audio-mood.xml` | audio | — | 2:00 loop | Hero ambience bed (long-form video, invitation film) |
| VLN-AUD-02 | `05-audio-mood.xml` | audio | — | 1:30 | Gathering — film trailer cue (brand film, event recaps) |
| VLN-AUD-03 | `05-audio-mood.xml` | audio | — | 0:45 loop | Tension / engine cue (ENGINE film, velocity b-roll) |
| VLN-AUD-04 | `05-audio-mood.xml` | audio | — | 1–8s each | Design layer library — stingers and textures |
| VLN-SOC-01 | `06-social-teasers.xml` | video | 9:16 | 8s | Reels / TikTok — "They chose sides." |
| VLN-SOC-02 | `06-social-teasers.xml` | video | 9:16 | 7s | Reels / TikTok — "The mask is not a disguise." |
| VLN-SOC-03 | `06-social-teasers.xml` | video | 9:16 | 8s | Reels / TikTok — "We stopped trading hours for money." |
| VLN-SOC-04 | `06-social-teasers.xml` | video | 9:16 | 10s | Reels / TikTok — "You can't come back." |
| VLN-SOC-05 | `06-social-teasers.xml` | video | 9:16 | 8s | Reels / TikTok — "There was a room." |
| VLN-SOC-06 | `06-social-teasers.xml` | video | 9:16 | 7s | Reels / TikTok — "They asked what we do all day." |

Pack `00-brand-bible.xml` produces no assets of its own. It is the master style contract —
palette, lighting doctrine, lens and film-stock language, composition rules, wardrobe, motifs,
the universal negative list, and the `<style_suffix>` string that every other prompt already
has appended to it. If a bot drifts off-look mid-session, re-paste the style suffix and the
universal negatives and regenerate.

---

## How to use these

Open the pack that owns the asset you want, find the `<asset>` block by its `id`, and copy the
entire contents of `<prompt>` into your image or video bot. The prompt strings are already
complete — the style suffix, the lighting doctrine and the palette hexes are baked into each
one, so you do not need to assemble anything. Paste `<negative_prompt>` into the bot's negative
field; in Midjourney, convert it to `--no term, term, term`, and note that the Midjourney prompts
already carry `--style raw` and the correct `--ar`. For video tools, generate a still first with
the matching look and drive image-to-video where the tool supports it — Runway and Kling both hold
the brand far better from an approved start frame than from text alone. Read the `<notes>` block
before you burn credits: it names the specific failure mode for that shot (cyan pool lights,
manufacturer badges, extra fingers on the mask hand, hallucinated chart imagery in the engine
loop) and tells you when to discard a take instead of trying to fix it.

Then save the output next to `index.html` as `assets/<ASSET-ID>.jpg` for stills or
`assets/<ASSET-ID>.mp4` for motion — for example `assets/VLN-IMG-05.jpg` or `assets/VLN-VID-01.mp4`.
Nothing else is required. The page's media loader reads the `data-asset` attribute on every slot
and probes `.jpg`, `.png`, `.webp` for stills and `.mp4`, `.webm` for video, in that order; the
first file that loads replaces the placeholder card automatically, so assets appear as you drop
them in and there is no manifest to edit. Export stills at 2400px on the long edge, sRGB, JPEG
quality 82–88, with no output sharpening. Export video as H.264 MP4, `yuv420p`, faststart, 24fps,
**no audio track** (hero and b-roll play muted and looped), targeting under 8 MB per loop. The
emblem itself is existing art at `assets/team-villain.png` — pack 04 generates only backplates
and treatments to sit it on, never the mark itself. Audio from pack 05 is not consumed by the
website; it is for edited films and social cutdowns, where the type is always set in post and
never generated.
