# Four words for testing a trading rule: no-information run, held, reserve, planted pattern

_A plain glossary of four ideas that separate a trading rule that repeats from one that only fitted noise._

Four words come up whenever someone asks whether a trading rule is real or only fitted noise. Here is each one in plain language.

## No-information run

A repeat of the whole test with the knowledge taken out. The same history, the same costs, the same scoring and the same search, but the signals carry no information: they are shuffled, or drawn at random. What it scores is how good "nothing" looks on that history. A rule that does not stand clear of it has shown nothing yet. More: https://telegra.ph/How-good-does-nothing-look-Why-a-backtest-needs-a-no-information-baseline-11-20

## Held

A stretch of history kept apart while a rule is being chosen. No setting is picked on it and no choice is made on it. It exists to judge a rule that was chosen somewhere else, because the history that judges a rule should never be the history that chose it.

## Reserve

A second stretch kept apart, and looked at last of all. Once you have looked at a held stretch and changed something because of what you saw, that stretch has started to choose for you. Reserve is the part that is still unseen when every other decision has been made. More: https://telegra.ph/Train-test-held-reserve-why-one-hold-out-is-not-enough-once-you-have-looked-at-it-11-20

## Planted pattern

A test of the tester. A known pattern is put into a made-up market, and that market is pushed through the same pipeline that judges real rules. The pipeline has to find what was planted. Then the planted pattern is scrambled, and the pipeline has to come up empty. A tester that fails either half cannot be trusted on real prices. More: https://telegra.ph/Test-the-instrument-before-you-trust-the-reading-planting-a-known-pattern-11-20

These four are how Ultimate Trading System, the software we build, is put together. Each run is repeated with votes that carry no information. Its sealed layout splits history four ways: train, test, held and reserve. And each release shows whether it has passed the planted-pattern check. The free trial needs no exchange account, and the work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
