# Prompt Anatomy

Most AI music prompts fail for the same reason: they describe a *feeling* but not a *recording*.

`a sad song about losing someone` gives the model nothing to hold onto — no instrument, no tempo, no voice, no production era. The model fills those blanks with whatever is statistically average in its training data, which is why so many generations sound like the same mid-tempo piano ballad.

This page describes the five-slot framework used throughout this repository, and the rules of thumb that come with it.

---

## The five slots

Every reliable style prompt fills these five slots. Order matters less than coverage — but the order below is what most models parse most predictably.

| # | Slot | Answers | Examples |
|---|------|---------|----------|
| 1 | **Genre** | What kind of music is this? | `Pop`, `Lo-fi`, `Stadium rock`, `Bossa nova` |
| 2 | **Mood** | What should the listener feel? | `Melancholic`, `Triumphant`, `Restless` |
| 3 | **Vocal** | Who is singing, or nobody? | `Female vocal`, `Male vocal`, `No vocals`, `Whisper` |
| 4 | **Tempo** | How fast, and how does it move? | `90 BPM`, `Slow`, `Half-time groove` |
| 5 | **Production** | What does the recording sound like? | `Tape saturation`, `Wide reverb`, `Dry close-mic drums` |

Slot 5 is the one most people skip, and it is the one that separates a generic result from a specific one. It is where you encode instrumentation, texture, mix character, and era.

### Filled in

```
Lo-fi, nostalgic, no vocals, 78 BPM, dusty piano loop, vinyl crackle, soft tape saturation
```

Five slots, 88 characters, no ambiguity about what should come out.

---

## Style tags vs. description

Most AI music tools give you two separate inputs, and they do different jobs. Using the wrong one for the wrong content is the second most common mistake after skipping slot 5.

| Input | What it is for | What it is *not* for |
|-------|----------------|----------------------|
| **Style / tags field** | Sonic attributes — the five slots above. Comma-separated fragments. | Narrative, story, subject matter |
| **Description / lyrics prompt** | Subject matter, story, point of view, what the song is *about* | Instrument lists, BPM, mix notes |

Putting `a song about my grandmother's kitchen` in the style field wastes characters the model will mostly ignore. Putting `120 BPM with sidechained pads` in the description field asks a lyric-oriented input to carry production information it was not built to route.

Keep them separated and both inputs get sharper.

---

## Seven rules of thumb

**1. Concrete beats evaluative.**
`warm` and `beautiful` are opinions. `tape saturation`, `close-mic acoustic guitar`, `no cymbals` are instructions. Models act on the latter.

**2. Budget your characters.**
Most tools cap the style field somewhere between 120 and 200 characters (MuseGen's limit is 180). Under that cap, fragments compete with each other — every tag you add dilutes the weight of the others. Five to nine well-chosen tags outperform twenty vague ones.

**3. Two or three genre words maximum.**
`Pop, rock, EDM, folk, jazz` does not produce a fusion. It produces mush, or the model silently picks one. If you want a hybrid, name it as a hybrid: `folk-electronica`, `jazz-inflected R&B`.

**4. Name the instrument that carries the song.**
Every arrangement has one element the listener follows. Say which one: `fingerpicked acoustic guitar`, `Rhodes piano`, `808 sub`. This single tag does more work than three mood adjectives.

**5. Anchor the tempo with a number when it matters.**
`Fast` spans 130–180 BPM depending on genre. If the track has to sit under a video cut or match a reference, give a number.

**6. Use negative tags to remove, not to steer.**
`no vocals`, `no distortion`, `no drums` are reliable. `not boring`, `not generic` are not — the model has no vector for those. See [negative-prompts.md](../prompts/negative-prompts.md).

**7. Change one slot at a time.**
When a generation is close but wrong, resist rewriting the whole prompt. Swap one slot, regenerate, compare. You will learn what each tag actually does far faster, and you will keep the parts that were already working.

---

## A worked example

Starting point — vague, evaluative, no production information:

```
sad emotional song, beautiful, touching
```

**Add genre and the carrying instrument** (slots 1 and 5):

```
Piano ballad, melancholic, sparse felt piano
```

**Add vocal and tempo** (slots 3 and 4):

```
Piano ballad, melancholic, female vocal, 68 BPM, sparse felt piano
```

**Add production character and one removal:**

```
Piano ballad, melancholic, female vocal, 68 BPM, sparse felt piano, close-mic breathy delivery, room reverb, no drums
```

117 characters. Every word is an instruction, nothing is an opinion, and the result is repeatable — which matters more than any single generation, because a prompt you can reason about is a prompt you can fix.

---

## Where to go next

- [Genres](../prompts/genres.md) — ready-to-paste prompts across 12 genres
- [Moods](../prompts/moods.md) — the same genres re-colored by emotional intent
- [Vocals](../prompts/vocals.md) — voice types and how to specify them
- [Tempo & structure](../prompts/tempo-and-structure.md) — BPM reference and song-form control
- [Use cases](../prompts/use-cases.md) — prompts organized by what you are making
- [Negative prompts](../prompts/negative-prompts.md) — removing what you don't want

---

<sub>Maintained by the [MuseGen](https://www.musegen.ai/) team. Prompts are tool-neutral — see the [compatibility notes](../README.md#compatibility).</sub>
