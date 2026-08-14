# Contributing

Contributions are welcome and the bar is deliberately low. You do not need to be a producer, and you do not need to open a big PR — one good prompt is a perfectly good contribution.

---

## What's useful

| Contribution | Notes |
|--------------|-------|
| **A new prompt** | The main thing. See the format below |
| **A fix** | A prompt that doesn't produce what it claims — tell us, or fix it |
| **Tool-specific findings** | "This needs adjusting on X" is genuinely valuable and under-supplied |
| **A new use case** | Something the [use-cases](prompts/use-cases.md) page doesn't cover |
| **Translations** | See [below](#translations) |

## What isn't

- Prompts that are only adjectives (`epic emotional beautiful song`)
- Duplicate entries that differ by one synonym
- Promotional links to tools or services, in prompts or in prose
- Reformatting or restructuring PRs without a discussion first

---

## Prompt format

Every entry follows the same shape. Copy this:

````markdown
### Genre — Variant name

**Style tags**

```
Comma-separated fragments, under 180 characters
```

**Description**
> What the song is about. One or two sentences.

**Why it works** — one sentence on the single thing this prompt does that a vague version wouldn't.

`NNN chars`
````

### The three requirements

**1. Specific.** A reader should be able to predict roughly what comes out. Name at least one instrument and one production characteristic. If every word could apply to half the library, it's not ready.

**2. Annotated.** The *why it works* line is not optional — it is what makes this a reference rather than a list. Point at one decision and explain it. "Sounds good" is not an explanation.

**3. Within limits.** Style tags must fit 180 characters, which is the tightest common cap across major tools. Count them (`echo -n "..." | wc -c`) and put the real number in the `NNN chars` line.

### Tested, please

Run your prompt at least once before submitting. If it didn't produce what the entry claims, it isn't ready — and if it produced something *better* than you expected, say what surprised you in the *why it works* line. That is often the most useful sentence on the page.

---

## Style conventions

- **British or American spelling** — either is fine, don't change existing entries to match your preference
- **Sentence case for headings**, except genre and proper nouns
- **No exclamation marks** in prose
- **Descriptions should be concrete.** "A song about loss" is weak; "a room being emptied by people being careful with each other" is what we're going for. Specificity in the description is the point of the description
- **No brand names in prompts** — `Rhodes` and `telecaster` are instrument categories and fine; a plugin name is not

---

## Translations

Translations are welcome and are the easiest way to contribute meaningfully.

- **README goes in the repository root** as `README.<lang-code>.md` — e.g. [`README.zh-CN.md`](README.zh-CN.md). That is the GitHub convention and it is where readers look first. Add a language switcher line above the `# ` heading in both files
- **Everything else goes in `translations/<lang-code>/`**, mirroring the top-level structure
- **Translate the prose, keep the style tags in English.** Most models are trained predominantly on English music description, and English tags currently produce more reliable results regardless of the target language. Note this in the translated file
- Partial translations are fine — one file is better than none
- If you translate `genres.md`, feel free to add genres specific to your language's music culture. That is a real improvement, not scope creep

---

## Submitting

1. Fork, branch, edit
2. Keep the PR focused — one section or one theme
3. In the PR description, say which tool you tested on
4. Open it. There is no template and no checklist to satisfy

Not sure whether an idea fits? Open an issue and ask. That is cheaper than writing something that gets turned down.

---

## Code of conduct

Be straightforward and don't be a jerk. Disagreement about whether a prompt works is fine and expected — that's most of what this repository is for.

---

## License

By contributing you agree that your contribution is released under the [MIT License](LICENSE), the same terms as the rest of the repository.
