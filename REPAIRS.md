# REPAIRS — the ilo chair

Written 2026-09-26 16:43, while the burn was at 14,139 of 23,213. Companion to
`NOTES.md`: NOTES records what was learned, this records what must be fixed.

## The sorting criterion, and it is the whole value of this file

**A repair is DETERMINISTIC when the token pair — the Hebrew surface plus the
wrong gloss — determines the right answer without reading the verse.**

Everything else is a **RE-PRESS**: the verse must go back through the chair,
because deciding it needs the sentence, the context, or a word nobody has chosen
yet.

That line matters because the two have completely different costs. A
deterministic repair is a script over 23,213 JSON files and runs in under a
minute for nothing. A re-press costs a model call per verse and shares the one
bulk lane with whatever is burning. **Sorting the list correctly is the
difference between an hour and a week**, and the sorting can only be done while
the findings are fresh — which is why this file is written during the burn and
not after it.

---

## A · DETERMINISTIC — a script, no judgement, no model call

### A1 · The seven substituted numbers
The only class in the corpus that can be graded arithmetically (exp 1018).
Match on the verse and the exact gloss; every one of these is a wrong integer.

| verse | surface | gloss now | must be | why |
|---|---|---|---|---|
| exodus/7/7 | `שמנים` | `ennem a pulo` | `walopulo` | Moshe was **80**, not 60 |
| exodus/7/7 | `ושמנים` | `ken innem a pulo` | `ken walopulo` | Aharon **83** |
| numbers/4/48 | `ושמנים` | `ken walo nga innem a pulo` | `ken walopulo` | **8,580** |
| exodus/38/26 | `וחמשים` | `ken tallopulo` | `ken limapulo` | census **603,550** |
| 1-kings/14/21 | `עשרה` | `ken duapulo` | `sangapulo` | Rehavam reigned **17** |
| numbers/7/3 | `עשר` | `duapulo` | `sangapulo ket dua` | **twelve** oxen |
| 1-samuel/17/17 | `ועשרה` | `ken uppat a pulo` | `ken sangapulo` | **ten** loaves |

**The flow must be repaired with the row.** A number fixed in the token list and
left wrong in the translation is worse than not fixing it, because the two
surfaces then disagree and the reader sees the flow.

### A2 · The Name with a suffix — spelling only
Every one of these is a string-for-string fix on the divine name. There is no
context in which any of them is right.

- `elohim mo` · `elohim-mo` → **`Elohimmo`** (73)
- `elohim yo` · `elohim-yo` → **`Elohimyo`** (43)
- `elohim yoyo` · `elohimyoyo` · `diosyoyo` → **`Elohimyo`** (18) — the suffix
  written twice
- `elohemyo` · `elohemayo` · `elohimo` · `elohimm` · `elohimmak` · `elohik` ·
  `elohimk` · `eloahko` · `elohuak` · `ngelohimmo` · `elohimnayo` ·
  `elohimyokayo` · `elohimyokadagiti` · `elohimpay` → the correct person-form
- `elohim yoyo` where the Hebrew is `אלהיך` → **`Elohimmo`** (a plural suffix on
  a singular)

### A3 · The Name itself — two letter-slips
- genesis/18/33 `ni Yahwey` → **`ni Yahweh`** (h → y)
- jeremiah/26/12 `Yawhweh` → **`Yahweh`** (hw transposed)
- psalms/31/15 `Yakweh` → **`Yahweh`** (h → k)

**THE NAME'S FAILURE MODE IS TYPOGRAPHIC, NEVER THEOLOGICAL.** Three slips in
**5,612 seats** — 99.91% — and every one is a single wrong or transposed character
inside a transliterated proper noun. **Not one is a substitution.** `Apo` ·
`Panginoon` · `Dios` · `Jehova` · `Lord` · `God` — the whole class the rails exist
to forbid — has never appeared, and the gate's own erasure line reads 0 verses.
A chair can mistype the Name; this one has never once replaced it. **Nothing else in the Name column
needs touching** — the erasure scan is zero, and the 181 `dios` glosses are the
chair correctly refusing to transliterate a false god (NOTES §53).

### A4 · The doubled derivational prefix
- `kinanalinteg` → **`kinalinteg`** (16) — `kina` + `na` + `linteg`

### A5 · The dropped particle
- `anak tao` → **`anak ti tao`** — *son of man* without its particle. The two
  SEMANTIC forbids (`anak a lalaki ti tao`, `anak ni Adan`) went to zero and
  stayed there; this one is the near-miss that drifted and settled at roughly
  two in five.

### A6 · Spelling variants with one right answer
- `upat a pulo` → **`uppat a pulo`** (4)
- `toram` → **`torah`**
- `asam` · `asamna` → the asham form, **once A-list target is chosen** (see C1)

### A7 · The Iberian letters — strip the diacritic
**62 verses and still climbing** (gate 45; it was 51 at gate 41). Written Ilocano
carries no stress marks, and stripping is also right on the transliterated names:
`Lehí` → `Lehi`.

**THIS WAS PINNED TWICE AND IT BELONGS HERE, NOT IN THE RAILS.** First at 16:14 as
a forbid on the characters; when four escaped, I read them, found `estaño` and
`allá` among them, and concluded at 17:16 that *a forbid on a character cannot fix
a word-choice, because the chair chooses words* — and re-pinned on the Spanish
**source** instead.

**That was half right, and the half I got wrong was to treat the deeper cause as
REPLACING the surface one instead of joining it.** The word-level pin worked: no
`estaño`, no `allá`, no `plomo`, no `Davíd` since. But seven more diacritics landed
after it, and **not one of them is a Spanish word**:

    18:17 psalms/78/8    espírituna.
    18:20 psalms/88/11   pelpelá,
    18:27 psalms/119/29  isuérannakomi;
    18:38 proverbs/14/3  amáwan
    18:46 job/3/13       nakdégak
    18:51 job/20/29      kenniña
    18:53 job/20/12      dilaña.

`dilaña` is the Ilocano `dilana`, *his tongue*, with `ñ` written for `n`.
`nakdégak` and `espírituna` are Ilocano words wearing an acute. **These are not
lexical choices at all — they have the shape of decoding noise on a single
character**, which is the same ruling already made for the non-Latin script class:
*decoding-level, no more rails rows.*

**So: two pins spent on it, the second one an over-correction, and the conclusion
is that the rails were the wrong instrument from the start.** It is a
`str/replace` over the corpus and it should have been one at 16:14.

### A3b · The Name DROPPED, not mistyped
- proverbs/21/31 `וליהוה` → **`ngem kenni`** — *but safety is of YHWH*. The
  preposition survived and **the Name fell out of the gloss.**

This joins Exodus 15:23 and 15:24 (both wholly empty) as the third of its kind, so
the Name's six faults split **three letter-slips and three drops**. A drop cannot
be scripted — the surrounding words are right and only the Name is absent — so it
is really a re-press, but it is listed here beside its siblings because anyone
fixing A3 will want all six in one place.
- `á é í ó ú ü` → `a e i o u u`
- **EXCEPT `ñ`** — `ngañ elohimmo` and `idiñaonda` are not words with or without
  the tilde, so they go to C (re-press), not here.

### A8 · The token-pair repairs — deterministic BECAUSE the surface is present
These need no verse read, because the Hebrew is sitting in the same token.
- surface `עם`-family + gloss contains `tattao` → **`ti umili`** (303–306, all
  pre-pin)
- surface `קדש`-family + gloss `nasantoan` → **`nasantuan`** (95–98, all pre-pin)
- **surface `בינה`-family + gloss containing `pannakaammo` → `pannakaawat`** (~24).
  `pannakaammo` is `דעת`'s word, from the root `ammo`, *to know*; `בינה` is
  `pannakaawat`, from `awat`, *to grasp*. **Forty-five of the family's sixty-six
  occurrences were pressed before the pin landed** — Proverbs and Job burned
  through in the twenty minutes it took to find the fault, tally it and write the
  rule. Also in this sweep: `kaungan` (*innermost*), `panunot` (*thought*), and the
  non-words `naan-ammo` · `nakaammo` · `makaan-am`.
  **The pinned form is proved on the hardest verse it will ever meet** —
  **Daniel 2:21, in Aramaic**: `ti agited ti kinasirib kadagiti nasirib ken ti
  pannakaammo kadagiti ammo iti pannakaawat` — *he giveth wisdom unto the wise, and
  knowledge to them that know understanding* — **five words, three roots, all
  separated, seven minutes after the pin and across a language boundary.**

---

## B · DETERMINISTIC BUT NEEDS ONE DECISION FIRST
The repair is mechanical the moment a single word is chosen. **The choice is
Scott's, not the shovel's** — see `questions-for-scott.md`.

### B1 · `propeta` vs `profeta`, and `propeta` vs `padto`
60 verb occurrences in 48 forms, five stems. **Haggai 1:3 reads `ti propeta` and
Haggai 2:10 reads `ti profeta` — same clause, nine verses apart**, so the corpus
has no preference to defer to. Once a stem is named, every one of the 48 forms
maps onto it mechanically.
Forbidden either way, and these ARE deterministic now: `naqil` · `manaqil` ·
`dimnaqilak` (not Ilocano words) · `agtapon` (*to leap*) · `agmumurlat`.

### B2 · `אלהיכם` joined or spaced
43 `elohim yo` against 43 `elohimyo` — a dead tie. The rails broke it on
paradigm consistency (if `אלהיך` is joined, so is `אלהיכם`), and A2 above assumes
the joined form. **If Scott prefers spaced, A2 inverts and `Elohimmo` goes with
it** — one decision, both columns.

---

## C · RE-PRESS — the verse must go back through the chair

### C1 · `asham` — 39 distinct forms in 62 tokens
The worst scatter in the corpus by rate, and **deliberately not pinned**: only
five of the 64 occurrences were still ahead, so a rails row would have cost every
remaining verse to save five. The tail holds **six different ways to say
guilt-offering**, because אשם is both *guilt* and *the guilt-offering* and Ilocano
splits them (`basol` / `daton`). A target form has to be chosen by ear, and then
the 62 re-press. **This is the cleanest example of why the sorting criterion
matters: the fault is severe, the ahead-count is nil, and the fix is cheap only
after the burn.**

### C2 · `goel` — ANSWERED BY THE CORPUS, 19:05, when Ruth landed

**This section predicted the chair might settle it itself, and it did.** Ruth holds
**19 occurrences and 15 are on the `goel` stem**, inflected as a living Ilocano
verb in nine different shapes nobody supplied: `aggoelenna` (*he will redeem it*) ·
`nga aggoel kennaka` · `goellem` (*redeem thou it*) · `magoel` (*can be redeemed*) ·
`ti goelna` (*his right of redemption*) · `kadagiti goeltayo` · and `ti goel` ·
`a goel` · `iti goel` as the plain title.

**And the four exceptions are all in Ruth 4:6 — the one verse where the kinsman
REFUSES**, where the chair switched to the native `tubbot`:

> `Kinuna **ti goel**: Saanak a makabael **nga agtubbot** a kas iti bagiak … 
> **tubbotenmo** sika ⟨את⟩ **ti tubbotko**, ta saanak a makabael **nga agtubbot**.`

**The man keeps the title; every act of redeeming he declines takes the native
word.** Ruth 3:13 is the counterpart with the act *accepted* and the verb stays on
the stem: `no ti goel ti **aggoel** kennaka — nasiayaat, **aggoelenna**`.

**Whether the chair meant that is unknowable. That it did it is measurable**, and
it is the same phenomenon as `goelenna` built unasked at Jeremiah 31:11 — here done
nine ways across one book. **So `goel` needs no pin: the corpus chose, and it chose
a transliterated noun with a native verb beside it.** What remains for a native ear
is only whether that split is right, which is a much smaller question than the one
this section opened with. Filed.

### C2-old · the pre-Ruth `goel` scatter — 14 forms in 32 tokens
`ti mangibales` (*the avenger*) · `agbabawi` (*repents*) · `nagsalakan`
(*saved*) · and **`ti kabagian a mangala-para`, *the kinsman who takes for*** —
the chair writing a definition because Ilocano has no noun for the
kinsman-redeemer. **Ruth is ahead and Ruth is the book of the goel**; watch what
lands there before choosing, because the chair may settle it itself.

### C3 · The empty glosses
- exodus/15/23 and exodus/15/24 — `ליהוה` glossed **empty**. The Name is
  missing, not wrong; nothing can be substituted in without the verse.
- joel/2/13 — `וקקרעו`, a **doubled qof in the surface itself**, with an empty
  gloss. The flow has the sense (*rend your heart*); the row lost the token.

### C4 · The notation and script leaks
- 37 verses with a non-Latin script outside `⟨ ⟩` (Chinese, Cyrillic)
- the homoglyphs — Cyrillic `а` inside otherwise perfect Ilocano words
- `ngañ` · `idiñaonda` — not words with or without the tilde
- `— saan:` (the chair arguing with itself in the verse), `∅`, `a(n)ga` (both
  alternates shipped), mixed `⟨…>>` brackets, verses ending in `...`

### C5 · The fabricated ⟨את⟩ — 16
The marker placed where the Hebrew has no `את`: joshua/10/37, genesis/17/25
(`בהמלו`), jeremiah/12/5 (`תתחרה`), jeremiah/27/12 (`ועמו`), exodus/15/22
(`יכלו`), exodus/12/38 (`עלה`) and others. **⟨את⟩ has lost NOTHING in 7,337
seats** — the fault is entirely in the other direction, and a fabricated marker
must be removed by reading, because the token it sits on is a real word that
still needs its gloss.

### C6 · `tao` for `איש` — flag, do not auto-replace
Ten in the Twelve and more behind. **It cannot go in list A**, because `איש` in
the distributive sense — *each one, every man* — is legitimately `tunggal maysa`,
and eight of the twenty-four non-`lalaki` renderings in the Twelve are that. A
blanket surface-`איש`-plus-gloss-`tao` replacement would overwrite correct work.
**This is the counter-example that defines the criterion: the token pair is
present and still does not determine the answer.**

### C6b · The three `ti tao` inside the pin's latency window
The `איש` pin went into the rails at **16:41:49** and the discipline caches were
cleared in the same call. The next three `איש` in Psalms still came out `ti tao` —
**psalms/5/7 at 16:43:54 · psalms/4/3 at 16:45:08 · psalms/1/1 at 16:48:03** —
and every `איש` from 16:49 onward is correct (`tunggal maysa` · `iti lalaki` ·
`lalaki`).

**So a pin has a LATENCY of roughly six to seven minutes, or eighty to a hundred
verses, even though the cache clear is instantaneous.** Calls already in flight
and calls already prompted carry the old rails. Nothing is wrong with the pin;
these three verses simply predate its effect.

They go here rather than in list A for the C6 reason — the distributive `איש` is
legitimately `tunggal maysa`, so no blanket replacement is safe — but all three
are plainly the plain noun and each is a one-word fix on reading.
**`psalms/1/1` is the one to fix first: it is the first verse of the Psalter.**
*Blessed is the man that walketh not in the counsel of the ungodly* → `ti tao`
should be `ti lalaki`.

### C7 · The one-letter slips that land on a real word
- exodus/7/7 `בדברם` → `idi saanda` (*when they did NOT*) for *when they spoke* —
  `sao` became `saan`
- deuteronomy/11/15 and 6/11 `ושבעת` → `ken agbusor ka` / `ken makabusor` (*and
  thou becomest an ENEMY*) for *and thou shalt be FULL* — `nabsog` became
  `busor`. 8:10 and 8:12 got it right as `napnoka`.

**None of these is detectable as a misspelling — only as a wrong meaning** — so
none can be found by a spell-check and none can be fixed without the verse.

---

## What is NOT on this list, and why

- **the 181 `dios` glosses** — the chair reserving the transliteration for the
  One. Correct. (NOTES §53)
- **`רוח`'s 107 non-`Espiritu` glosses** — branched by rule into `anges` and
  `angin`. Correct, and Ezekiel 37 took all three branches in one chapter.
- **`שבת`'s 52 non-`Shabbat` glosses** — noun and verb; the verb is `inana`.
- **`hesed` at Leviticus 20:17** — `makaddakes a banag`, *a wicked thing*, the
  one verse in the Tanakh where the word means its opposite. **Do not
  "correct" this to `hesed`.** It is the proof the chair is reading.
- **`kadua` for `עם`** — that is `עִם`, *with*. Correct.
- **`dagitoy` for `אלה`** — that is `אֵלֶּה`, *these*. Correct, all 28.
- **`tunggal maysa` for `איש`** — the distributive. Correct.
- **the 672-verse LOOPS reading list** — Ilocano is agglutinative and a repeated
  word is usually one possessive suffix; demoted from fault to reading list after
  eighteen were read and eighteen were right.

**Six of these were things a probe accused and a reading acquitted.** Anything
added to this file from here on gets read first.


---

# §11 · THE HAND PASS — the thirty-five, each decided against the en floor

Written 2026-09-26 21:45, after §10 took the census from 628 to 74 and the
floor-anchoring took it to 35. **The runbook's rule is *decided against the en
floor, never guessed*, and reading these is where three more of my own probe's
convictions collapsed.**

## Fillable — 15 empty glosses, now DETERMINISTIC because the floor names the word

The row has a hole and the flow usually reads fine, which is why nothing looked
wrong. The floor supplies the sense and the Ilocano is standard:

| verse | Hebrew | en floor | fill |
|---|---|---|---|
| genesis/42/21 | `על` | concerning | `maipapan iti` |
| genesis/42/21 | `הזאת` | this | `daytoy` |
| genesis/46/18 | `עשרה` | -teen | `sangapulo ket` |
| jeremiah/44/14 | `אם` | except | `malaksid` |
| jeremiah/25/8 · 2-kings/18/12 · numbers/20/24 | `אשר` | that | `a` |
| 2-chronicles/18/17 | `אם` | only | `no saan` |
| 1-samuel/2/27 | `אליו` | to him | `kenkuana` |
| ezekiel/5/6 | `בהם` | in them | `kadakuada` |
| 2-kings/15/12 | `לך` | for you | `kenka` |
| numbers/7/84 ×3 | `עשרה` `עשר` `עשרה` | ten | `sangapulo` |
| 2-samuel/21/7 | `בשת` | son of | part of `Mephiboshet` — a tokenisation seam |

## HELD — 2, and the reason is that the FLOOR IS EMPTY TOO

- **job/38/37** — `יסספר`, a **doubled samekh**. Not a Hebrew word. **en has no
  gloss either.**
- **1-kings/20/28** — `ויאא`. Not a Hebrew word. **en has no gloss either.**

**The chair is not at fault in either: the SOURCE TOKEN is malformed, and both
chairs hit it identically.** That is an OSHB-side seam, not a rendering fault, and
it is the first thing in this whole file that belongs to neither the chair nor the
rails.

## HELD — 1 fabricated marker, and three chairs have now arrived at it

- **daniel/3/12** — `יתהון` → `⟨את⟩`. **Aramaic's own object marker.** `xh`'s
  re-press script holds this exact seat as *"awaits the Aramaic ruling"*, and `sv`
  and `cs` both reached it the same way. **Four chairs, one unanswered question.**
  Not the chair's fault; the project's.

## Removable — 4 fabricated markers, deterministic (no `את` in the Hebrew)

| verse | Hebrew | en floor | why |
|---|---|---|---|
| proverbs/28/11 | `יחקרנו` | will search him out | the `-nu` is an object SUFFIX, not the marker |
| 2-kings/14/19 | `וימתהו` | and put him to death | the `-hu` is an object suffix |
| 2-chronicles/35/22 | `אל` | to | a preposition |
| 2-chronicles/8/18 | `אוניות` | ships | a plain noun |

**Two of the four are the את-family logic stretched one step too far** — a
pronominal object *suffix* is not the object *marker*, and the rails' own
את-family rule (which rightly covers `אתו` · `אתי` · `אתך`) does not reach `-nu`
or `-hu`.

## CLEARED BY READING — the `goel` eight, and my matcher was wrong again

| verse | ilo | verdict |
|---|---|---|
| psalms/74/2 | `tinubbotmo` | **CORRECT — `tubbot` with the `-in-` infix** |
| isaiah/52/9 | `tinubbotna` | **CORRECT — same** |
| deuteronomy/19/6 | `ti mangibales` | **CORRECT — this is the `goel ha-dam`, the AVENGER of blood** |
| leviticus/27/20 ×2 · 25/54 | `maibayad` · `mabayadan` | defensible — Leviticus' redemption-PRICE sense |
| psalms/77/16 · exodus/15/13 | `bumuyodam` · `binawimo` | genuinely unclear; held for an ear |

**`tinubbotmo` contains the `tubbot` stem with Ilocano's completed-aspect infix
`-in-`, and my exclusion regex looked for the bare stem.** That is the same fault
as scoring `lallaki` a failure because the plural reduplicates — **an agglutinative
target inflects INSIDE the word, and a matcher anchored on the bare stem will
convict its own pin.**

And Deuteronomy 19:6's `mangibales` is the sharpest of them: `גֹּאֵל הַדָּם` is the
**avenger** of blood, not the redeemer — the same root doing the opposite office.
The chair knew.

## What the hand pass leaves

**19 deterministic** (15 fills + 4 marker removals) → a second §9 run.
**3 held** (two malformed source tokens, one Aramaic ruling).
**2 for an ear** (psalms/77/16, exodus/15/13).
**11 defensible or cleared.**

**Of the thirty-five, eleven were the chair being right.** Of the seventy-four
before the floor-anchoring, **forty** were.
