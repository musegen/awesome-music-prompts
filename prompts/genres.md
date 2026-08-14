# Genre Prompts

Twelve genres, three variants each. Every variant is a genuinely different production choice, not a synonym swap — the point is to show the range inside a genre, not to pad the list.

New here? Read [Prompt Anatomy](../docs/prompt-anatomy.md) first.

**Jump to:** [Pop](#pop) · [Rock](#rock) · [Hip-Hop](#hip-hop) · [R&B](#rb) · [EDM](#edm) · [Folk](#folk) · [Jazz](#jazz) · [Lo-fi](#lo-fi) · [Guofeng](#guofeng) · [Metal](#metal) · [Classical](#classical) · [Country](#country)

---

## Pop

### Pop — Radio Anthem

**Style tags**

```
Pop, triumphant, female vocal, 122 BPM, punchy four-on-the-floor drums, bright synth stabs, wide layered chorus
```

**Description**
> A song about the first morning after quitting a job you hated — relief that hasn't turned into fear yet.

**Why it works** — `wide layered chorus` tells the model where the energy peak belongs. Without it, pop prompts tend to produce verses that never resolve into a hook.

`111 chars`

---

### Pop — Bedroom Pop

**Style tags**

```
Bedroom pop, wistful, soft male vocal, 96 BPM, muted electric guitar, warm bass, tape hiss, no big drums
```

**Description**
> Watching a neighbourhood change from a window you've looked out of for ten years.

**Why it works** — `no big drums` is doing the heavy lifting. Bedroom pop is defined as much by restraint as by instrumentation, and models default to full kits unless told otherwise.

`104 chars`

---

### Pop — Synth-Pop Throwback

**Style tags**

```
Synth-pop, nostalgic, male vocal, 118 BPM, analog synth bass, gated reverb snare, arpeggiated pads, 1984
```

**Description**
> A letter to someone you only ever knew through late-night phone calls.

**Why it works** — `gated reverb snare` and the year `1984` are era anchors. A single concrete decade marker shifts the whole mix character more reliably than the word "retro".

`104 chars`

---

## Rock

### Rock — Stadium Anthem

**Style tags**

```
Stadium rock, defiant, male vocal, 138 BPM, overdriven guitars, crowd-sized chorus, live room drums, big toms
```

**Description**
> Standing in a town you swore you'd leave and realising you still know everyone's name.

**Why it works** — `live room drums` prevents the sterile close-mic sound that AI rock defaults to. Room character is what makes rock read as *played* rather than programmed.

`109 chars`

---

### Rock — Garage Rock

**Style tags**

```
Garage rock, restless, raw male vocal, 152 BPM, fuzz guitar, driving eighth-note bass, dry drums, minimal reverb
```

**Description**
> Four people in a van who have not agreed on anything for six hundred miles.

**Why it works** — `minimal reverb` plus `dry drums` forces the close, cramped sound garage rock depends on. Left unsaid, the model will smooth it into modern alt-rock.

`112 chars`

---

### Rock — Alt-Rock Slow Burn

**Style tags**

```
Alternative rock, brooding, male vocal, 84 BPM, clean arpeggiated guitar into distortion, dynamic build, half-time drums
```

**Description**
> A conversation that both people know is the last one, conducted entirely about something else.

**Why it works** — `clean … into distortion` describes an arc, not a state. Prompts that encode change across the track produce far more interesting structure than static descriptions.

`120 chars`

---

## Hip-Hop

### Hip-Hop — Boom Bap

**Style tags**

```
Boom bap hip-hop, gritty, male rap vocal, 92 BPM, dusty chopped soul sample, hard swung drums, upright bass, vinyl noise
```

**Description**
> An account of a corner store that stayed open through three recessions and one fire.

**Why it works** — `swung` is the single most important word here. Straight-quantised boom bap sounds mechanical, and the swing feel is rarely applied unless requested explicitly.

`120 chars`

---

### Hip-Hop — Trap

**Style tags**

```
Trap, cold, male vocal with ad-libs, 140 BPM, 808 sub bass, rapid hi-hat rolls, sparse dark piano, heavy sidechain
```

**Description**
> Counting a night's takings in a car park at 4am and feeling nothing about it.

**Why it works** — `140 BPM` with `rapid hi-hat rolls` gives the half-time feel trap needs. Naming the ad-libs separately keeps the vocal from being rendered as a single flat take.

`114 chars`

---

### Hip-Hop — Jazz Rap

**Style tags**

```
Jazz rap, contemplative, laid-back male vocal, 88 BPM, Rhodes piano, brushed drums, walking upright bass, muted trumpet
```

**Description**
> Reading old letters you wrote and not recognising the person who wrote them.

**Why it works** — Naming four specific instruments crowds out the generic trap palette models reach for by default. In hybrid genres, instrumentation is the strongest steering signal.

`119 chars`

---

## R&B

### R&B — Slow Jam

**Style tags**

```
R&B slow jam, sensual, female vocal, 68 BPM, Rhodes chords, deep round bass, finger snaps, lush background harmonies
```

**Description**
> Two people who keep almost saying the thing, over the course of one long evening.

**Why it works** — `lush background harmonies` is the genre's signature and one of the few vocal-arrangement instructions models follow well. Say it or you get a single dry lead.

`116 chars`

---

### R&B — Neo-Soul

**Style tags**

```
Neo-soul, warm, female vocal, 76 BPM, loose unquantised drums, extended jazz chords, wurlitzer, organic live feel
```

**Description**
> A Sunday afternoon in a house where four generations have cooked in the same kitchen.

**Why it works** — `loose unquantised drums` is the technical description of neo-soul's behind-the-beat feel. It moves the result far more than adding another mood adjective.

`113 chars`

---

### R&B — Alt-R&B

**Style tags**

```
Alternative R&B, hazy, androgynous vocal, 72 BPM, pitched vocal samples, sub bass, cavernous reverb, minimal percussion
```

**Description**
> Describing a city you've left to someone who has never been there, and getting it slightly wrong on purpose.

**Why it works** — `minimal percussion` plus `cavernous reverb` creates the negative space alt-R&B is built on. The genre is defined by what is absent.

`119 chars`

---

## EDM

### EDM — Festival Drop

**Style tags**

```
Big room EDM, euphoric, no vocals, 128 BPM, supersaw lead, filtered build, white noise riser, four-on-the-floor kick
```

**Description**
> Instrumental — built for the moment a crowd realises what track is starting.

**Why it works** — `filtered build` and `white noise riser` name the transition devices explicitly. Drops fall flat when the model has no instruction about what precedes them.

`116 chars`

---

### EDM — Deep House

**Style tags**

```
Deep house, hypnotic, no vocals, 122 BPM, warm analog bassline, dusty chord stabs, shuffled hats, long filter sweeps
```

**Description**
> Instrumental — a room that has been full for hours and will be for hours more.

**Why it works** — `long filter sweeps` encodes patience. Without it, house prompts get compressed into pop-length arcs with a chorus-shaped section every thirty seconds.

`116 chars`

---

### EDM — Melodic Techno

**Style tags**

```
Melodic techno, tense, no vocals, 124 BPM, rolling bassline, detuned arpeggio, dark pads, sparse ride, gradual build
```

**Description**
> Instrumental — a long drive through an industrial district before sunrise.

**Why it works** — `gradual` and `rolling` set expectations about pacing. Techno lives on slow parameter change, which needs stating because most training data rewards fast payoff.

`116 chars`

---

## Folk

### Folk — Acoustic Storyteller

**Style tags**

```
Acoustic folk, plain-spoken, male vocal, 94 BPM, fingerpicked steel-string guitar, upright bass, brushed snare, no reverb
```

**Description**
> A man who repaired the same stretch of fence every spring for forty years and never explained why.

**Why it works** — `no reverb` puts the singer in the room with the listener. Intimacy in folk is a mixing decision, and models add space unless told not to.

`121 chars`

---

### Folk — Indie Folk Build

**Style tags**

```
Indie folk, hopeful, mixed vocals, 108 BPM, acoustic guitar, group harmonies, stomps and claps, building to full band
```

**Description**
> Everyone you grew up with, in one room, one last time, and nobody mentions it.

**Why it works** — `building to full band` describes the arc that defines this style. Static prompts produce a track that starts full and stays there, which misses the point entirely.

`117 chars`

---

### Folk — Sea-Shanty Stomp

**Style tags**

```
Sea shanty, rowdy, male chorus, 116 BPM, accordion, fiddle, stomping boots, unison group vocals, no drum kit
```

**Description**
> A crew arguing about a route while every one of them already knows the answer.

**Why it works** — `no drum kit` forces the percussion into stomps and claps, which is what makes a shanty sound like a shanty rather than folk-rock with an accordion.

`108 chars`

---

## Jazz

### Jazz — Swing Standard

**Style tags**

```
Jazz swing, playful, female vocal, 132 BPM, walking upright bass, brushed drums, muted trumpet, piano comping
```

**Description**
> A running joke between two people that stopped being funny and became a greeting.

**Why it works** — `comping` is the correct term for what a jazz pianist does behind a soloist, and models trained on music text respond to it. Genre-native vocabulary consistently beats plain description.

`109 chars`

---

### Jazz — Cool Jazz Ballad

**Style tags**

```
Cool jazz, melancholic, no vocals, 62 BPM, muted trumpet lead, brushed kit, sparse piano, upright bass, late-night club
```

**Description**
> Instrumental — the last forty minutes of a bar's night, from behind the counter.

**Why it works** — `sparse` is essential. Jazz prompts without a density instruction produce busy bebop-adjacent results regardless of the tempo you asked for.

`119 chars`

---

### Jazz — Bossa Nova

**Style tags**

```
Bossa nova, breezy, soft female vocal, 128 BPM, nylon-string guitar, light shaker, subtle flute, gentle syncopation
```

**Description**
> Someone describing a place they have decided not to return to, fondly.

**Why it works** — `nylon-string` rather than "acoustic guitar" is the difference between bossa nova and folk. One word of specificity resolves an entire genre ambiguity.

`115 chars`

---

## Lo-fi

### Lo-fi — Study Loop

**Style tags**

```
Lo-fi hip hop, calm, no vocals, 78 BPM, dusty piano loop, soft boom bap drums, vinyl crackle, tape saturation
```

**Description**
> Instrumental — designed to be ignored, which is the hardest thing to write.

**Why it works** — `designed to be ignored` is the real design constraint. `vinyl crackle` plus `tape saturation` supply the texture that makes the loop bearable at hour three.

`109 chars`

---

### Lo-fi — Rainy Night

**Style tags**

```
Lo-fi, wistful, no vocals, 72 BPM, Rhodes chords, muted trumpet, rain ambience, slow swung drums, low-pass filter
```

**Description**
> Instrumental — a window seat, a long wait, no particular hurry.

**Why it works** — `low-pass filter` is what "muffled" actually means in production terms. Naming the process rather than the impression gets a far more consistent result.

`113 chars`

---

### Lo-fi — Lo-fi Soul

**Style tags**

```
Lo-fi soul, warm, distant female vocal, 84 BPM, chopped soul sample, dusty drums, warm bass, heavy tape wobble
```

**Description**
> A half-remembered song from a house you lived in once.

**Why it works** — `distant` positions the vocal in the mix rather than describing its tone — lo-fi vocals sit behind the instruments, and mix position is the thing to specify.

`110 chars`

---

## Guofeng

*Guofeng (国风) is contemporary Chinese music built on traditional instrumentation and melodic modes. It is under-represented in most English-language prompt collections, and models respond well to instrument names given specifically.*

### Guofeng — Wuxia Epic

**Style tags**

```
Guofeng, majestic, female vocal, 96 BPM, guzheng, dizi flute, taiko-style drums, sweeping strings, pentatonic melody
```

**Description**
> A promise made on a mountain road that both parties intend to keep and neither can.

**Why it works** — `pentatonic melody` is the structural instruction that makes this read as Chinese rather than as Western orchestral music with a guzheng on top.

`116 chars`

---

### Guofeng — Jiangnan Ballad

**Style tags**

```
Guofeng ballad, tender, soft female vocal, 68 BPM, pipa, erhu, bamboo flute, light water percussion, spacious mix
```

**Description**
> Rain on a stone bridge, and a name nobody has said out loud in years.

**Why it works** — `pipa` and `erhu` together produce a distinctly southern Chinese timbre. Naming two traditional instruments rather than one prevents the arrangement collapsing into a single exotic accent.

`113 chars`

---

### Guofeng — Guofeng Electronic

**Style tags**

```
Guofeng electronic, dramatic, female vocal, 130 BPM, guzheng over 808 bass, trap hats, orchestral hits, modern mix
```

**Description**
> Old myth, new city, same argument.

**Why it works** — `guzheng over 808 bass` states the fusion as a layering relationship. Listing both palettes flatly tends to make the model choose one; describing which sits on top gets both.

`114 chars`

---

## Metal

### Metal — Melodic Death

**Style tags**

```
Melodic death metal, ferocious, harsh male vocal, 168 BPM, twin harmonized guitars, blast beats, double kick, minor key
```

**Description**
> A structure collapsing exactly as predicted, watched by the person who predicted it.

**Why it works** — `twin harmonized guitars` is the genre's defining feature and rarely appears without being named. `harsh` prevents a clean-sung result.

`119 chars`

---

### Metal — Doom

**Style tags**

```
Doom metal, oppressive, low clean male vocal, 62 BPM, downtuned sludgy guitars, slow crushing drums, thick fuzz bass
```

**Description**
> A winter that has gone on long enough to stop being a season and start being a condition.

**Why it works** — `62 BPM` is the instruction. Metal prompts pull toward fast tempos by default, and doom only works if the tempo is stated numerically and low.

`116 chars`

---

### Metal — Metalcore Anthem

**Style tags**

```
Metalcore, cathartic, screamed verse clean chorus, 172 BPM, chugging breakdown, double kick, soaring lead, big production
```

**Description**
> Saying the thing you have rehearsed for a year, to someone who left before you could.

**Why it works** — `screamed verse clean chorus` encodes the genre's central vocal contrast in one fragment, and cleanly separates the two deliveries by section.

`121 chars`

---

## Classical

### Classical — String Adagio

**Style tags**

```
Classical strings, mournful, no vocals, 58 BPM, string orchestra, slow swelling dynamics, minor key, concert hall reverb
```

**Description**
> Instrumental — a room being emptied by people who are being careful with each other.

**Why it works** — `swelling dynamics` asks for volume change over time, which is where string writing lives. Static classical prompts produce flat, sample-library results.

`120 chars`

---

### Classical — Solo Piano Nocturne

**Style tags**

```
Solo piano nocturne, intimate, no vocals, 66 BPM, expressive rubato, sustain pedal, close-mic felt piano, no other instruments
```

**Description**
> Instrumental — playing quietly at night because someone else in the house is asleep.

**Why it works** — `no other instruments` is necessary. Ask for solo piano and models still tend to add strings by the second minute unless the exclusion is explicit.

`126 chars`

---

### Classical — Baroque Concerto

**Style tags**

```
Baroque concerto, stately, no vocals, 104 BPM, harpsichord continuo, chamber strings, counterpoint, ornamented melody
```

**Description**
> Instrumental — a procedure performed identically for two hundred years.

**Why it works** — `harpsichord continuo` and `counterpoint` are period-correct structural terms. They place the piece in the baroque far more reliably than the word "classical" ever will.

`117 chars`

---

## Country

### Country — Modern Nashville

**Style tags**

```
Modern country, warm, male vocal, 118 BPM, electric guitar with slide, tight drums, banjo accents, polished radio mix
```

**Description**
> A truck that has been sold three times within one family and is still running.

**Why it works** — `polished radio mix` separates modern country from its traditional forms, which is the ambiguity that sinks most country prompts.

`117 chars`

---

### Country — Outlaw Country

**Style tags**

```
Outlaw country, weathered, gravelly male vocal, 102 BPM, telecaster twang, upright bass, brushed snare, dry vintage mix
```

**Description**
> An unpaid debt that both parties have agreed to call a favour.

**Why it works** — `dry vintage mix` and `telecaster twang` supply the era and the instrument in five words. Vintage country is a production sound before it is a songwriting style.

`119 chars`

---

### Country — Country Ballad

**Style tags**

```
Country ballad, aching, female vocal, 72 BPM, pedal steel, acoustic guitar, soft brushed drums, close intimate vocal
```

**Description**
> A wedding attended alone, described entirely through what was on the tables.

**Why it works** — `pedal steel` is the single instrument that says "country ballad" unambiguously. One well-chosen instrument name outperforms three genre adjectives.

`116 chars`

---

## See also

- [Moods](moods.md) — the same palettes re-colored by emotional intent
- [Vocals](vocals.md) — voice types in detail
- [Tempo & structure](tempo-and-structure.md) — BPM reference by genre
- [Negative prompts](negative-prompts.md) — what to exclude

---

<sub>Maintained by the <a href="https://www.musegen.ai/">MuseGen</a> team · <a href="../CONTRIBUTING.md">Contribute a prompt</a></sub>
