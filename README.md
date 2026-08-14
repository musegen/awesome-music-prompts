**English** · [简体中文](README.zh-CN.md)

# Awesome Music Prompts

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Prompts](https://img.shields.io/badge/prompts-96-blue.svg)](prompts/)
[![Tool neutral](https://img.shields.io/badge/tool-neutral-lightgrey.svg)](#compatibility)

A curated, copy-pasteable prompt library for AI music generation — organized by genre, mood, vocal type, tempo, and use case.

Every prompt in this repository is written to a consistent five-slot structure, fits inside the character limits real tools impose, and comes with a short note explaining *why* it is built the way it is. The goal is not a pile of prompts to copy blindly, but a reference you can learn the grammar from.

---

## Why this exists

Search for AI music prompts and you mostly find two things: screenshots of prompts with no explanation, and lists of adjectives (`epic`, `emotional`, `beautiful`) that models largely ignore.

The problem is that vague prompts don't fail loudly — they fail by producing something *listenable but generic*. You get a competent mid-tempo track that sounds like everything else, and no signal about which word caused it.

This library takes the opposite approach:

- **Every prompt is specific enough to be repeatable.** Named instruments, real BPM values, explicit production character.
- **Every prompt is annotated.** A one-line *why it works* note, so you can adapt rather than only copy.
- **Every prompt respects real constraints.** Style fields are capped in most tools; these are written to fit.

---

## Quick start

Read [**Prompt Anatomy**](docs/prompt-anatomy.md) first — it's a five-minute read and it makes the rest of the library make sense.

The short version: a reliable style prompt fills five slots.

| Slot | Answers | Example |
|------|---------|---------|
| **Genre** | What kind of music? | `Lo-fi` |
| **Mood** | What should it feel like? | `Nostalgic` |
| **Vocal** | Who sings, or nobody? | `No vocals` |
| **Tempo** | How fast? | `78 BPM` |
| **Production** | What does the recording sound like? | `Dusty piano loop, vinyl crackle` |

Put together:

```
Lo-fi, nostalgic, no vocals, 78 BPM, dusty piano loop, vinyl crackle, soft tape saturation
```

Keep subject matter (*what the song is about*) out of the style field and in the description/lyrics field instead. They are different inputs and they route differently.

---

## Contents

| Collection | What's inside |
|------------|---------------|
| [**Genres**](prompts/genres.md) | 12 genres × 3 variants — Pop, Rock, Hip-Hop, R&B, EDM, Folk, Jazz, Lo-fi, Guofeng, Metal, Classical, Country |
| [**Moods**](prompts/moods.md) | 12 emotional registers, from cheerful to intense, each in two arrangements |
| [**Vocals**](prompts/vocals.md) | Female, male, chorus, child, whisper, harmony, and instrumental |
| [**Tempo & structure**](prompts/tempo-and-structure.md) | BPM reference by genre, and how to control song form |
| [**Use cases**](prompts/use-cases.md) | Podcast intros, game loops, ads, weddings, study beats, trailers, short-form video |
| [**Negative prompts**](prompts/negative-prompts.md) | What to exclude, and which exclusions actually work |
| [**Prompt anatomy**](docs/prompt-anatomy.md) | The framework and seven rules of thumb |

---

## Format

Every entry follows the same shape:

````markdown
### Genre — Variant name

**Style tags**

```
Comma-separated fragments that go in the style field
```

**Description**
> What the song is about — goes in the description or lyrics field.

**Why it works** — the one thing this prompt does that a vague version doesn't.

`87 chars`
````

The character count is there so you can see the headroom before you start editing.

---

## Compatibility

These prompts are **tool-neutral**. The five-slot structure is a property of how text-conditioned music models read input, not of any one product, so the entries here transfer across tools with minor adjustments.

They were written and checked against [MuseGen](https://www.musegen.ai/), whose style field caps at 180 characters and accepts comma-separated tags plus a separate negative-tag input. Every prompt here fits that cap, which is the tightest of the common limits — so they transfer without truncation.

Starting points for adapting to other tools. These are **suggestions, not test results** — corrections from people who have actually run them are exactly what this repo needs:

| Tool | Suggested adjustment |
|------|---------------------|
| Suno | Shorter style field — drop production tags first, keep genre + mood + vocal |
| Udio | Responds to era and reference-adjacent phrasing; try adding a decade tag |
| Stable Audio | Instrumental-first — the vocal slot is often a no-op, spend it on production |
| Riffusion | Prefers fewer, broader tags; try merging slots 4 and 5 |

If you test these on any tool, listed or not, [a PR with your findings](CONTRIBUTING.md) is genuinely useful.

---

## Contributing

New prompts, corrections, tool-specific findings, and translations are all welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

The bar for a new prompt is simple: it must be **specific** (a reader can tell what will come out), **annotated** (one line on why it works), and **within limits** (fits a 180-character style field).

---

## License

[MIT](LICENSE) — use these anywhere, commercially or otherwise, no attribution required.

Note that the license covers *this collection*. Whether the music you generate is commercially usable depends on the terms of the tool you generate it with — check those separately.

---

<sub>Maintained by the <a href="https://www.musegen.ai/">MuseGen</a> team. If this saved you some trial and error, a ⭐ helps others find it.</sub>
