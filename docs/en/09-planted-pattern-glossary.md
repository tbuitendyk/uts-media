# A word for testing a trading rule: the planted pattern

_Before trusting a search that says it found a rule, check that it can find one you hid on purpose. What a planted pattern is, and how to use one._

Every check on this list so far asks whether a rule is real. This one asks something earlier: can the search find a real rule at all?

## What it means

A planted pattern is a rule you put into a made-up market on purpose. You build prices that follow a known pattern, mixed with noise, so that you know the right answer before you start. Then you run the whole search on that market, exactly as you would on real history, and see whether it finds what you hid.

## Why it matters

A search that never fails is not proof of anything. If the machinery has a fault, it can report rules that are not there, or miss rules that are. On real history you cannot tell which, because nobody knows the right answer. On a made-up market you do. A search that cannot find a pattern you planted cannot be trusted when it says it found one you did not.

## How to use it

Plant a pattern, run the real pipeline over it, not a shortcut, and check that it is found. Then scramble the same made-up market so the pattern is destroyed, run it again, and check that nothing is found. Both halves count: finding the pattern shows the search can see; coming up empty on the scrambled copies shows it does not see things that are not there. Run the check again whenever the software changes.

## Where it sits among the other checks

It comes first, before any rule is judged: test the instrument, then trust the reading. After it come how good "nothing" looks, history the rule never saw, and the simpler ways of trading the same stretch.

## Where we use it

Ultimate Trading System, the software we build, plants a known pattern in a made-up market and pushes it through the real pipeline, which must find it while scrambled versions of it come up empty. Each release shows whether it has passed. There is no AI in what runs, and the same inputs give the same answer every time. The free trial needs no exchange account, and the work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

Testing the instrument first, at length: https://telegra.ph/Test-the-instrument-before-you-trust-the-reading-planting-a-known-pattern-11-20

The word before this one, the simpler way: https://telegra.ph/A-word-for-testing-a-trading-rule-the-simpler-way-11-24

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
