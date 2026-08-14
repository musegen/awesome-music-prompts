# Negative Prompts

Negative prompts remove things. They do not steer, persuade, or improve — and confusing those two functions is why most negative prompts do nothing.

Some tools have a dedicated negative-tag field. Where there isn't one, the same fragments work inline in the style field (`no drums`, `no vocals`), though usually with slightly less force.

---

## The rule

**A negative prompt works when it names a thing that could be present in the audio.**

`drums` is a thing. `distortion` is a thing. `boring` is not a thing — there is no acoustic feature the model can remove to satisfy it.

| Works | Does nothing |
|-------|--------------|
| `no drums` | `not boring` |
| `no vocals` | `not generic` |
| `no distortion` | `not cheesy` |
| `no reverb` | `high quality` |
| `no fade out` | `not amateur` |
| `no brass` | `professional` |
| `no autotune` | `not bad` |

The right-hand column is not merely useless — it consumes characters that could have carried a real instruction, and in a 180-character field that cost is real.

---

## Reliable exclusions

### Instrumentation

| Fragment | Use when |
|----------|----------|
| `no drums` | Ballads, ambient, solo instrumental — the single most useful exclusion |
| `no percussion` | Broader than `no drums`; also removes shakers, tambourine, claps |
| `no bass` | Sparse, floating arrangements |
| `no guitar` | Prevents guitar creeping into piano or electronic pieces |
| `no brass` | Cinematic prompts that keep turning into trailer music |
| `no strings` | Solo piano pieces that keep growing an orchestra |
| `no synths` | Enforcing an all-acoustic arrangement |
| `no orchestral elements` | Keeping intimate pieces intimate |
| `no other instruments` | Genuine solo performance — strongest form |

### Vocals

| Fragment | Use when |
|----------|----------|
| `no vocals` | Standard instrumental request |
| `no voice at any point` | Stronger — use when `no vocals` still produces vocal pads |
| `no wordless vocals` | Removes "ooh/aah" pads specifically, a very common leak |
| `no rap` | Hip-hop-adjacent prompts that should stay sung |
| `no screaming` | Heavy prompts that should stay clean |
| `no autotune` | Modern pop and hip-hop where you want a natural voice |
| `no backing vocals` | Keeping a single dry lead |

### Production

| Fragment | Use when |
|----------|----------|
| `no reverb` | Intimacy — puts the source in the room with the listener |
| `no distortion` | Clean electric tones |
| `no sidechain` | Electronic tracks where pumping is unwanted |
| `no heavy compression` | Preserving dynamic range |
| `no lo-fi effects` | Preventing vinyl crackle appearing uninvited |
| `no tape hiss` | Clean modern production |
| `no harsh transients` | Sleep, relaxation, ambient |

### Structure & arrangement

| Fragment | Use when |
|----------|----------|
| `no fade out` | You need a clean edit point — very commonly needed |
| `no ending` | Loop material |
| `no big drop` | Background music that shouldn't grab attention |
| `no key change` | Preventing the final-chorus modulation cliché |
| `no solos` | Ambience, retail, background |
| `no tempo changes` | Sync work where the grid must stay fixed |
| `no silence at the start` | Avoiding dead air you'd have to trim |

---

## Common problems and their fixes

**"I asked for instrumental but got humming."**
`no vocals` frequently leaves wordless vocal pads, since the model doesn't classify them as vocals. Use `no vocals, no wordless vocals, no voice at any point`. Three overlapping exclusions is justified here — this is the most persistent leak in AI music generation.

**"My solo piano piece grew an orchestra by the second minute."**
Models associate emotional escalation with added instruments. `no other instruments` plus `solo performance throughout` fixes it. `throughout` is the operative word — it constrains the whole timeline, not just the opening.

**"Everything fades out and I can't cut it."**
`no fade out, clean ending` — worth adding by default to anything destined for video, since fades are painful to edit around.

**"My lo-fi track is too clean / my clean track has vinyl crackle."**
Lo-fi texture tags leak between genres because they co-occur so often in training data. `no lo-fi effects, no vinyl crackle, clean modern production` for the second case.

**"The background music keeps stealing attention."**
`no big drop, no solos, even dynamics, no sudden changes`. Background music is defined almost entirely by what it doesn't do.

**"The metal track isn't heavy enough."**
This is *not* a negative-prompt problem. Nothing needs removing — you need positive tags: `downtuned`, `double kick`, `wall of sound`, `dense distorted guitars`. Reaching for negatives when the fix is positive is the most common misuse.

---

## How many is too many

Negative tags compete with positive ones for the model's attention. Past roughly four, they start suppressing things you wanted.

| Count | Verdict |
|-------|---------|
| 1–2 | Ideal. Usually all you need |
| 3–4 | Fine when they target one persistent problem (e.g. the vocal leak) |
| 5+ | Diminishing returns; often produces thin, empty results |

A prompt that is half negatives is usually a prompt whose positive half was never specific enough. **Fix the positive side first.** Most problems that look like "the model added something I didn't want" are really "the model had a blank to fill, and filled it."

---

## Ready-made sets

**Clean instrumental**

```
no vocals, no wordless vocals, no voice at any point
```

**Editable for video**

```
no fade out, no silence at the start, clean ending
```

**Seamless loop**

```
no ending, no fade out, no tempo changes
```

**Unobtrusive background**

```
no big drop, no solos, no sudden changes
```

**Intimate and dry**

```
no reverb, no drums, no other instruments
```

**Sleep-safe**

```
no percussion, no harsh transients, no sudden changes
```

---

## See also

- [Prompt anatomy](../docs/prompt-anatomy.md) — rule 6 covers when to reach for a negative at all
- [Vocals](vocals.md) — the instrumental section
- [Use cases](use-cases.md) — per-context constraints

---

<sub>Maintained by the <a href="https://www.musegen.ai/">MuseGen</a> team · <a href="../CONTRIBUTING.md">Contribute a prompt</a></sub>
