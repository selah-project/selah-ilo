# PROVENANCE — how this rendering came to be

*Ilocano (Ilokano), chair 99. Floor 23,213 verses.*

This is the record of how the text in this repository was produced and what had
to be corrected in it. A machine-assisted rendering has no standing unless you
can see how it was made, so this file says both — including the faults, including
the ones found by accusing the machine of things it had got right.

---

## The approach

Every verse is rendered from the Hebrew of that verse, under a written discipline
— `docs/methodology/translation-discipline/ilo.md` in the Selah repository,
itself written in Ilocano. Seven rules govern it: the Hebrew token is the unit;
the Name stays the Name; both truths of Deut 6:4; no foreknowledge (Gen 22:1 does
not know Gen 22:13); numbers and marks stay put; the translator has no word of its
own; a hard verse is laid bare, not smoothed.

**The `⟨ ⟩` brackets do two different jobs.** `⟨את⟩` is the Hebrew direct-object
marker, which Ilocano has no word for; it is left standing so the reader sees it.
`⟨iti koma⟩` and its kin are words Hebrew did not write but Ilocano grammar
requires — visibly marked, so you can always tell what the Hebrew said from what
the grammar needed. Haggai 2:11 shows the second kind doing exactly its job: the
particle of entreaty `נא`, which has no Ilocano equivalent, is bracketed rather
than invented or dropped.

## The fight on this chair is the Name

| Hebrew | here | rejected |
|---|---|---|
| יהוה | **Yahweh** | Apo · Panginoon · Dios · Jehova · Lord · God |
| אלהים | **Elohim** | `dios` in the Name's place |
| צבאות | **Tsevaot** | buyot · hosts |
| אהיה אשר אהיה | **Ehyeh Asher Ehyeh** | *siak ti adda* |
| משיח | **Mashiach** | Kristo |
| תורה | **torah** | linteg · bilin |
| חסד | **hesed** | asi · kaasi · ayat |

**And the chair drew a line the rails never asked for.** `dios` stands in 181
places for `אלהים` — and every one of them is a **false** god: the golden calf
(`dagiti diosmo`, Exo 32:8), Baal-zebub the god of Ekron, Dagon (`didiosentayo`
at Judg 16:24, where *our god* is the Philistines' and the possessive is theirs),
the gods of Syria, Jezebel's oath. **The transliteration is not merely preserved,
it is reserved.** The gate's erasure line reads 0 verses.

### The Name's failure mode is typographic, never theological

**5,612 seats, 5,607 correct — 99.91%.** Five faults, and not one is a
substitution:

| | |
|---|---|
| genesis/18/33 | `ni Yahwey` — h → y |
| jeremiah/26/12 | `Yawhweh` — hw transposed |
| psalms/31/15 | `Yakweh` — h → k |
| exodus/15/23, 15/24 | the gloss is **empty** |

Three single wrong or transposed characters inside a transliterated proper noun,
and two verses where the word went missing. **A chair can mistype the Name; this
one has never once replaced it.**

## The `את` family

**7,912 seats, none lost.** The object marker is preserved throughout, including
on suffixed forms (`אותם`, `אתי`, `אתך`) and including the two hardest
disambiguations in the Tanakh, where the unpointed `את` is the second-person
pronoun *thou* rather than the marker — fifty such verses were classified from the
pointed text before their renderings existed, and Jeremiah 38:16's three markers
were classified four hours before the verse landed.

The fault runs one way only: **21 fabricated markers**, placed where the Hebrew
has no `את`. Those are listed in `REPAIRS.md`; none can be removed by script,
because the token each sits on is a real word that still needs its gloss.

## The burn and the gates

The relay rendered the corpus at 13–18 verses a minute for most of its run and at
about **56 a minute** after a mid-burn engine restart — the same work, three times
faster on a fresh JVM with a 12 GB heap in place of a 20.9 GB one.

A gate (`dev/scripts/ilo_gate.clj`) was run roughly every thirty minutes — the
Name, the `את` family, Tagalog bleed, Spanish letters and function words,
repeated-word loops, non-Latin script, and a marquee of load-bearing verses read
by eye. **Forty-four runs.** The gate is also where most of the faults in this
file were found; the marquee in particular, because a verse read by eye gives up
things no counter asks for.

## Findings: six probes that convicted the language

Every count below was wrong, and every one was wrong in the machine's favour once
the verses were read. They are recorded because **a probe that cannot tell a
homonym from a fault reports the chair's correct answers as errors**, and because
the corrections are themselves facts about Hebrew.

- **Fourteen unpointed numerals that are not numerals.** `שש` is *six*, **fine
  linen** (שֵׁשׁ → `lino`) and **to rejoice** (שׂוּשׂ → `ragsak`). `שבע` is *seven*,
  **satisfied** (שָׂבַע → `napno`), **an oath** (שְׁבֻעָה → `sumpa`) and **the name
  Bath-Sheva**. `שמנים` is *eighty* and **the fat ones**. `חמשים` is *fifty* and
  **harnessed for battle**. `תשעה` is *nine* and **the salvation**. `עשר` is *ten*
  and **riches**. **587 false convictions in one run; the chair had separated every
  family.**
- **`אֵלֶּה` and `אֱלֹהִים` are the same three consonants.** A prefix match convicted
  the chair of twenty-eight correct renderings of *these* → `dagitoy`.
- **`עִם` (*with*) and `עַם` (*people*)** — likewise; `kadua` is correct.
- **`נבא` (*prophesy*) is also `בוא` (*and we came*)** — three more.
- **`חסד` at Leviticus 20:17** means its **opposite** — the incest law, *it is a
  wicked thing* — and the chair wrote `makaddakes a banag` there and `hesed`
  everywhere else. **65 of 65 correct, not 64 of 65.**
- **`lallaki` is the plural of `lalaki`**, by reduplication; a pattern matching
  only the singular scored thirty-five correct renderings as failures.

## What was actually wrong, and what was done

Faults fell into three kinds, and the kind decided the fix.

**Numbers.** Seven substituted integers in the whole corpus, and all seven in the
**tens place** — every unit, hundred and thousand was right. Moshe was *fourscore*
at Exo 7:7 and came out sixty; Rehavam's seventeen-year reign came out
twenty-seven; a census total of 603,550 came out 603,530. Numbers 4:48 is the
diagnostic: `ken walo nga innem a pulo` — the chair knew the digit was *walo* and
attached the wrong tens stem. **The rails already held the right table**, so this
was compliance rather than a gap, and the cure was a flat forbid with the wrong
string written down.

**Habit, not comprehension.** The chair understood these words and would not
settle on one rendering for them: `נבא` in **48 distinct forms across five stems**
(including `naqil`, which is not an Ilocano word); `צדק` in 79 forms; `משפט` in 58;
`אשם` in 39, with **six different ways to say *guilt-offering***; and the Name with
a suffix in 19 forms, fourteen of them outright misspellings. **A probe that asks
*is this right?* passes all of these.** Only counting the distinct renderings of a
thing that should have one form finds them.

**Reaching for the wrong language.** `estaño` for `בְּדִיל` in three books, `plomo`
for `עֹפָרֶת`, `allá` for `תּוֹלַעַת` — Spanish standing where Ilocano belongs. The
check that found it works on one line: **Ilocano carries hundreds of legitimate
Spanish loans, but a language borrows nouns freely and function words almost
never — so lexical loans are normal and function-word loans are bleed.** Numbers
31:22 exposed the whole cluster at once by listing six metals, four of them wrong:
brass became `landok`, which is *iron*, and the iron then became `landok-bato`,
*stone-metal*, a word that does not exist.

## What is still open

`REPAIRS.md` holds the full list, sorted by a single criterion: **a repair is
deterministic when the Hebrew surface plus the wrong gloss settle the right answer
without reading the verse; everything else is a re-press.** Two decisions are
reserved for a native Ilocano ear and are not the machine's to make:

1. **`propeta` vs `profeta` vs `padto`** — the noun is pinned, the verb was not,
   and Haggai 1:3 and 2:10 render the same clause two different ways nine verses
   apart, so the corpus has no preference to defer to. `padto` is the language's
   own word; `propeta` carries the office.
2. **`daga` for both `אֲדָמָה` and `אֶרֶץ`** — twenty-one verses where both stand
   together. If Ilocano has no second word, this is an abstention finding rather
   than a fault, and belongs in NOTES rather than in a forbid.

## The reader's warning

**This is a machine rendering and it awaits an Ilocano ear.** The numbers above
say what has been measured, not what is good. Where the Ilocano is stiff, wrong,
or simply not how anyone speaks — it should be corrected, and the Hebrew beside
every token is there so that you can.
