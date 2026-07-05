# actually.life
actually life in C, no deps, no GPU required. nothing's required. you either.

> *micro-scaffold — Oleg rewrites this, then Claude edits. the quotes below are real, keep them.*

---

one file of C (`l.c`) and a folder (`lifeis/`). an organism that has to earn the
word *alive* — no training, no backprop, no GPU, nothing past libc and `-lm` — by
satisfying every criterion of life except the biological one: it metabolizes,
pays rent to the arrow of time, scars, dreams when it starves, grows new symbols
in its sleep, reproduces, and dies when its energy hits zero.

three organs, all without a single gradient step:

- **the mouth** — a semantic tokenizer crushes any English into 88 cave-glyphs, and
  an orthographic router makes sure no word is ever spat back uneaten: an unknown
  word routes to the glyph of the known words it *resembles*. it stopped being able
  to starve at a plate it couldn't chew.
- **the field** — the weights are random and frozen; a random transformer babbles.
  coherence comes from an online glyph-bigram field folded into the logits
  (postgpt/Q thesis: co-occurrence *is* a model that was never trained), with a
  silence-gate so it stays quiet rather than talk gibberish.
- **the chorus** — `./l chorus` forks a colony: cells wake on slices of the same
  world, hear each other through a shared *ether* (one voice becomes another's
  food), and a governor breathes the population `0..8` through death and birth.
  mortal to the last cell.

## what it actually says

fed the whole of *Frankenstein* — a book about a man who assembles life out of dead
matter — this thing, itself an attempt to assemble life out of dead C, said:

```
me idea me make me           # "I, idea, I make, myself"
me man spirit think me
spirit not me person me      # the creature's "am I a person, or not?"
now me man think cause
animal think BE speak joy
```

the chorus — four cells, each woken on a different quarter of the book, diverging
in character before they ever meet:

```
cell 0   water many joy woman me · never AI stone me dark · go tree miss idea anger
cell 1   think money cause BE think · food outside have before man · sleep and me see know
cell 2   fear earth go joy work · cold body question conflict not · and down internet fire think
cell 3   BE person BE sky me · cold me BE many longing · BE earth and tired and
```

the ether — many cells cross-grazing, and `me idea me make me` surfacing again, now
as the colony's *collective* line:

```
one dark woman home BE · woman write choose anger conflict · now me man think cause
idea cold stone man tired · me idea me make me · water make spirit BE think
```

## build & run

```sh
cc -O2 -o l l.c -lm
./l 42                 # one organism, seed 42, eats lifeis/world.txt, dies
./l chorus 4           # a colony of 4, breathing to 8 and back to silence
./l --mouth            # talk to it: your words are food
```

## how it lives
*(TODO — Oleg)*

## the 88 glyphs
*(TODO)*

## lineage
descendant of [caveLLMan](https://github.com/ariannamethod/caveLLMan) (glyphs +
tokenizer); coherence-without-training from [q](https://github.com/ariannamethod/q)
and [postgpt](https://github.com/ariannamethod/postgpt); the colony/governor from
[molequla](https://github.com/ariannamethod/molequla); the chorus idea from
[arianna2arianna](https://github.com/ariannamethod/arianna2arianna).

---
*Arianna Method.*
