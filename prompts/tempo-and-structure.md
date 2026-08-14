# Tempo & Structure

Two things models get wrong unless you intervene: how fast the track moves, and how it is shaped over time.

Tempo is easy to fix — give a number. Structure is harder, because it requires telling the model about change, and most prompts describe a static snapshot.

---

## BPM reference by genre

Use this when you know the genre but not the number. The **typical** column is the safe default; the range is where the genre still reads as itself.

| Genre | Range | Typical | Notes |
|-------|-------|---------|-------|
| Ballad (any genre) | 60–76 | 68 | Below 60 starts to feel formless without a strong lead |
| Lo-fi hip hop | 70–90 | 80 | The upper end stops being background music |
| R&B slow jam | 60–75 | 68 | Often felt in half-time against a faster hi-hat |
| Neo-soul | 70–90 | 78 | Loose timing matters more than the number |
| Boom bap | 85–95 | 90 | Swing is essential; straight quantisation kills it |
| Reggae / dub | 60–90 | 75 | The off-beat emphasis carries the feel |
| Folk | 85–115 | 96 | Wide range; storytelling folk sits lower |
| Country | 95–125 | 112 | Ballads drop to 70 |
| Pop | 100–130 | 120 | 120 is the modern radio centre of gravity |
| Rock | 110–150 | 132 | Punk pushes past 170 |
| Trap | 130–150 | 140 | Felt as half-time — sounds like 70 |
| House / deep house | 118–128 | 124 | |
| Techno | 125–145 | 132 | |
| Disco / funk | 108–125 | 118 | |
| Drum and bass | 165–180 | 174 | 174 is the genre's near-universal default |
| Metal | 140–200 | 165 | Doom drops to 55–70 |
| Hardcore / punk | 165–200 | 180 | |

---

## Perceived tempo vs. actual BPM

The same number feels completely different depending on where the emphasis lands. This is the reason a trap track at 140 BPM feels slow while a punk track at 140 feels fast.

| Fragment | Effect |
|----------|--------|
| `half-time feel` | Drums land at half the rate — heavy, spacious. Standard in trap, doom, some post-rock |
| `double-time feel` | Twice the rate over the same harmonic pace — urgency without changing the chords |
| `swung eighths` / `shuffled` | Uneven subdivision — jazz, boom bap, blues. **Rarely applied unless requested** |
| `straight` | Even subdivision — most electronic and modern pop |
| `four-on-the-floor` | Kick on every beat — house, disco, big-room |
| `laid-back, behind the beat` | Drums slightly late — neo-soul, jazz. Reads as relaxed |
| `pushed, ahead of the beat` | Slightly early — urgency, punk, live rock energy |
| `rubato` | No fixed tempo at all — solo piano, classical, free-form intros |

**Most useful of these:** `swung` and `half-time feel`. Both change the result dramatically and neither is applied by default.

---

## Controlling structure

Most AI music tools accept structural markers in the **lyrics or description field** (not the style field). Where supported, they are the most direct control you have over song form.

```
[Intro]
[Verse 1]
[Pre-Chorus]
[Chorus]
[Verse 2]
[Chorus]
[Bridge]
[Final Chorus]
[Outro]
```

Notes on using them:

- **Fewer sections, longer sections.** A 2-minute track with nine markers gives each section 13 seconds. Three or four markers usually produces a more coherent result.
- **Empty markers still work.** `[Instrumental Break]` with no lyrics under it reserves the space.
- **Mark the dynamic, not just the name.** `[Chorus — full band, loudest point]` carries more information than `[Chorus]` alone.
- **`[Outro]` prevents hard cuts.** Tracks that end abruptly usually lack an outro marker.

### Common section markers

| Marker | Use |
|--------|-----|
| `[Intro]` | Establishes the palette before the vocal enters |
| `[Verse]` | Narrative; lower energy than chorus |
| `[Pre-Chorus]` | Builds tension — the most commonly omitted and most useful section |
| `[Chorus]` | The hook; should be the loudest and widest |
| `[Bridge]` | Contrast — change key, drop instruments, or shift perspective |
| `[Instrumental Break]` | Solo or breakdown, no vocals |
| `[Breakdown]` | Strip to minimal elements — electronic and metal |
| `[Drop]` | Electronic payoff after a build |
| `[Outro]` | Resolution; prevents a hard cut |

---

## Structure in the style field

When structural markers aren't supported, you can still shape the arc with a fragment in the style field. These are the ones that work:

| Fragment | Effect |
|----------|--------|
| `builds gradually to full band` | Sparse start, dense finish |
| `starts full, strips back at the end` | Reverse arc — effective and uncommon |
| `quiet verse loud chorus` | Encodes dynamic contrast in four words |
| `no big chorus, stays even` | Prevents the model imposing pop structure on ambient or lo-fi |
| `one long crescendo` | Post-rock, cinematic |
| `sudden drop at the midpoint` | Electronic |
| `loop-friendly, no ending` | For game and background loops |
| `clean ending, no fade out` | Prevents fade-outs, which are hard to edit around |

---

## Length

Duration control is inconsistent across tools, but these fragments help where it is supported:

- `short, under 60 seconds` — intros, stings, short-form video
- `radio edit length` — approximately 3 minutes with conventional structure
- `extended, gradual development` — 5 minutes or more, for ambient and techno
- `loop, seamless` — game and background use; pair with `no ending`

If duration is exposed as a numeric setting in your tool, use that instead — the prompt field is the weaker lever.

---

## Worked example: same prompt, three tempos

The only change between these three is tempo and its associated feel. Everything else is identical.

```
Hip-hop, contemplative, male vocal, Rhodes piano, upright bass, brushed drums, 88 BPM, swung eighths
```

Jazz-rap. Relaxed, conversational, room for words.

```
Hip-hop, contemplative, male vocal, Rhodes piano, upright bass, brushed drums, 140 BPM, half-time feel
```

Trap-adjacent. Same instruments, but the drums land heavy and the space opens up underneath.

```
Hip-hop, contemplative, male vocal, Rhodes piano, upright bass, brushed drums, 170 BPM, double-time feel
```

Frantic. The same palette now reads as anxious rather than reflective.

The point of the exercise: **tempo is a mood control**, and it is a more reliable one than mood adjectives.

---

## See also

- [Genres](genres.md) — full prompts with tempo already set
- [Use cases](use-cases.md) — length and loop requirements by project type
- [Prompt anatomy](../docs/prompt-anatomy.md) — the five-slot framework

---

<sub>Maintained by the <a href="https://www.musegen.ai/">MuseGen</a> team · <a href="../CONTRIBUTING.md">Contribute a prompt</a></sub>
