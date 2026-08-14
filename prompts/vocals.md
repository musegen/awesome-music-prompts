# Vocal Prompts

The vocal slot is worth more characters than most people give it. `female vocal` describes a category; `breathy close-mic female vocal, restrained` describes a performance — and performance is what listeners actually respond to.

Two things to keep separate:

- **Voice type** — who is singing (this page)
- **Vocal placement** — where the voice sits in the mix (also this page, and frequently the more important of the two)

**Jump to:** [Female](#female-vocal) · [Male](#male-vocal) · [Chorus](#chorus) · [Child](#child-vocal) · [Whisper](#whisper) · [Harmony](#harmony) · [No vocals](#no-vocals) · [Placement](#vocal-placement) · [Delivery](#delivery-modifiers)

---

## Female vocal

**Powerful lead**

```
Pop, triumphant, powerful female vocal with belted chorus, 120 BPM, wide production, layered backing vocals
```

`107 chars` — `belted` specifies the technique. Without it, "powerful" tends to be rendered as louder rather than as a different vocal register.

**Restrained lead**

```
Indie folk, wistful, restrained female vocal, 84 BPM, close-mic, audible breath, acoustic guitar, no vocal effects
```

`114 chars` — `audible breath` is a small detail with outsized effect: it is the clearest marker of a real human at a real microphone.

---

## Male vocal

**Warm baritone**

```
Soul, warm, rich male baritone, 76 BPM, Rhodes, live drums, gospel-tinged phrasing, natural room sound
```

`102 chars` — Naming the range (`baritone`) rather than just the gender narrows the result considerably.

**Gritty rock lead**

```
Rock, defiant, gritty male vocal with rasp, 134 BPM, overdriven guitars, slight vocal distortion, live energy
```

`109 chars` — `rasp` and `slight vocal distortion` together produce wear without tipping into a scream.

---

## Chorus

**Group unison**

```
Folk anthem, communal, group unison vocals, 112 BPM, acoustic guitars, stomps, everyone singing the same line
```

`109 chars` — `unison` matters. Ask for a "chorus" and models often produce harmonized parts; unison singing has a completely different, rougher character.

**Gospel choir**

```
Gospel, uplifting, full choir with soloist, 88 BPM, Hammond organ, call and response, hand claps, big hall
```

`106 chars` — `call and response` gives the choir a structural role rather than making it a texture pad behind the lead.

---

## Child vocal

**Sing-along**

```
Kids sing-along, cheerful, child vocals, 116 BPM, ukulele, simple repeating melody, handclaps, bright and clear
```

`111 chars` — `simple repeating melody` matters as much as the voice. Children's music is defined by melodic economy.

**Innocent and quiet**

```
Lullaby, gentle, single child voice, 68 BPM, music box, sparse accompaniment, very soft, slightly imperfect pitch
```

`113 chars` — `slightly imperfect pitch` prevents the over-polished result that makes child vocals sound synthetic.

---

## Whisper

**Intimate ASMR-adjacent**

```
Ambient pop, intimate, whispered female vocal, 70 BPM, very close mic, minimal instrumentation, high detail, quiet
```

`114 chars` — `very close mic` is what makes a whisper legible. Whispers at a normal mic distance disappear into the mix.

**Tension**

```
Dark cinematic, unsettling, whispered layered voices, 62 BPM, low drone, no melody, whispers panned wide
```

`104 chars` — `panned wide` places whispers around the listener, which is where their unease comes from.

---

## Harmony

**Close harmony duet**

```
Indie folk, tender, two voices in close harmony, 82 BPM, acoustic guitars, both voices equal in mix, no lead
```

`108 chars` — `both voices equal in mix, no lead` prevents the default lead-plus-backing arrangement. Duets need this stated.

**Stacked lead harmonies**

```
Dream pop, hazy, stacked female harmonies, 98 BPM, wide reverb, chorus effect on vocals, no single dry lead
```

`107 chars` — `stacked` means one singer multiplied, which is a different texture from multiple singers. Worth distinguishing.

---

## No vocals

**Instrumental with a lead melody**

```
Cinematic, hopeful, no vocals, 90 BPM, solo cello carries the melody, strings underneath, no voice at any point
```

`111 chars` — Instrumental prompts often produce wordless vocal pads anyway. Naming which instrument takes the melodic role fills the space the voice would have occupied.

**Pure texture**

```
Ambient, calm, no vocals, 60 BPM, sustained pads, no melody, no percussion, no voice, background listening
```

`106 chars` — Stacking three exclusions is justified here: each removes a different default the model would otherwise supply.

---

## Vocal placement

Placement is a mix decision and often changes the emotional result more than voice type does. These fragments can be appended to any prompt on this page.

| Fragment | Effect | Fits |
|----------|--------|------|
| `close-mic` | Singer feels inches away, breath audible | Folk, ballads, ASMR-adjacent |
| `distant vocal` | Voice sits behind instruments | Lo-fi, shoegaze, dream pop |
| `buried in mix` | Voice as texture, lyrics semi-legible | Shoegaze, ambient pop |
| `dry vocal, no reverb` | Immediate, confrontational | Punk, hip-hop, garage |
| `cathedral reverb` | Vast, ceremonial | Choral, epic, ethereal |
| `doubled vocal` | Thicker, more confident | Pop, rock choruses |
| `telephone EQ` | Filtered, distant, degraded | Intros, verse contrast |

---

## Delivery modifiers

These describe *how* the line is sung. One well-chosen modifier usually beats two mood adjectives.

| Fragment | What it does |
|----------|--------------|
| `belted` | Full-voice, high energy, chorus-appropriate |
| `restrained` | Held back, implies withheld emotion |
| `breathy` | Air in the tone, intimate |
| `raspy` | Wear and texture, adds age |
| `spoken word` | Not sung at all — good for verses and bridges |
| `half-sung, half-spoken` | Conversational, common in modern indie and rap-adjacent pop |
| `melismatic` | Multiple notes per syllable — R&B, gospel, soul |
| `deadpan` | Flat affect; effective against emotional lyrics |
| `screamed` | Metal, hardcore, post-hardcore |
| `falsetto` | Above natural range, fragile |

**Combining:** delivery modifiers stack well with placement fragments, but stop at two. `breathy restrained close-mic doubled female vocal with rasp` is self-contradictory and the model will pick two at random.

---

## See also

- [Genres](genres.md) — full prompts with vocals already specified
- [Moods](moods.md) — emotional targets and how to reach them
- [Negative prompts](negative-prompts.md) — removing vocals reliably

---

<sub>Maintained by the <a href="https://www.musegen.ai/">MuseGen</a> team · <a href="../CONTRIBUTING.md">Contribute a prompt</a></sub>
