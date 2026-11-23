# A word for testing a trading rule: the sealed layout (train, test, held, reserve)

_Four parts of history, each with one job, so the history that judges a trading rule is never the history that chose it._

When someone asks whether a trading rule is real, the next question is always: real on which history? A sealed layout answers it by splitting history into four parts before anything is tried, each with one job.

## Train

The history the search learns from. Rules are fitted here, so a rule always looks good here. Nothing that happens on train counts as evidence.

## Test

The history used to choose between the rules the search produced. It is not the history they were fitted on, but it is still history a choice was made on. Once you have picked the best of many rules on test, test has started to flatter the winner.

## Held

History kept apart while every choice was being made. The rules that survive are judged here, against simpler ways of trading the same stretch. Held is the first honest reading, but only once: if you change something because of what held showed you, held has begun to choose too.

## Reserve

A last stretch, opened last of all, after every other decision is made. It is the part that is still unseen when nothing is left to adjust. A rule that holds up here has been judged on history no choice was ever made on.

## Why "sealed"

Because the parts are fixed before the work starts, and the later ones are not looked at early. Split history only two ways and look at the second part more than once, and you are back to choosing on the history that judges you.

## Where we use it

Ultimate Trading System, the software we build, splits history this way in its sealed layout: train, test, held and reserve. The history that judges a rule is never the history that chose it, and reserve is looked at last. Each run is also repeated with votes that carry no information, so you see how good "nothing" looks first. The free trial needs no exchange account, and the work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

Why one hold-out is not enough, at more length: https://telegra.ph/Train-test-held-reserve-why-one-hold-out-is-not-enough-once-you-have-looked-at-it-11-20

The word before this one, deterministic: https://telegra.ph/A-word-for-testing-a-trading-rule-deterministic-11-22

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
