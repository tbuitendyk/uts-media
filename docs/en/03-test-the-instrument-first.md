# Test the instrument before you trust the reading: planting a known pattern

_Before believing what a backtest says about real prices, check it on a made-up market where you already know the answer. How, and why it matters._

A backtest is a measuring instrument. A rule and some history go in, and a reading comes out. Most of the worry in testing goes to the rule: was it overfitted, was the history long enough. Much less goes to a plainer question. Does the instrument itself work?

It is a fair question, because a testing pipeline is software, and software has faults. The awkward part is that real history cannot tell you. If the pipeline says a rule is good, you have no separate way of knowing whether the rule is good or the pipeline is wrong. You do not know the right answer. That is why you are testing.

So before trusting it on real prices, give it a case where you do know the answer.

## A scale and a known weight

Nobody trusts a kitchen scale just because it shows a number. You put something of known weight on it and see whether it agrees. Then you take the weight off and check that it reads zero. The two checks catch different faults. A scale stuck at zero passes the second and fails the first. A scale that shows weight with nothing on it fails the second.

A testing pipeline can fail in the same two ways. It can be blind: something real is in the data, and it reports nothing. Or it can see things: nothing is in the data, and it reports a find. In trading the second is the dangerous one, because a find is what you were hoping for, and good news rarely gets checked twice.

## Planting a pattern, then scrambling it

The known weight, for a backtest, is a made-up market with a pattern hidden in it on purpose.

Start with prices made from coin flips: each hour up or down, with nothing connecting one hour to the next. No rule can find anything there, because there is nothing to find. Then plant something. For example, after three rises in a row, make the next hour rise more often than it falls. You chose the pattern, you know where it is, and you know how strong you made it.

Now push that made-up market through the pipeline. Not a simplified copy, and not a special test mode. The real one, start to finish, the same code that will later read real history. It must find what you planted.

If it does not, something is broken, and this is the cheap place to learn it. The usual causes are dull: signals lined up against the wrong hour, a step that quietly drops rows, a score worked out on the wrong column. Any of them can erase a real pattern. On real history you would simply have concluded there was nothing there.

That is half the test. For the other half, take the same made-up market and scramble it, so every up and down is still present but the order is shuffled. The pattern is gone. Push that through the same pipeline. This time it must come up empty.

If it still reports a find, the pipeline is seeing things. A classic cause is information leaking from the future: somewhere, the work for one hour was allowed a look at a later hour. A leak like that makes almost anything look good, noise included. In laboratory terms the planted market is a positive control and the scrambled one is a negative control. A result is believed only when both behave.

## What a pass is worth

Be clear about what this proves. It shows the instrument can see a pattern of the kind and strength you planted, and that it stays quiet when there is none. It says nothing about any particular rule found in real history, and nothing about what such a rule does next.

Two details decide whether the check means anything.

Plant something faint. A pattern as loud as a siren can be found even by a half-broken pipeline. Make it about as weak as what you would hope to find in real data.

Tie the pass to the code that earned it. Change the pipeline and the check has to be run again. Otherwise you are trusting a scale that has been taken apart and put back together since it was last checked.

In Ultimate Trading System, the software we build, the instrument is tested first. A known pattern is planted in a made-up market and pushed through the real pipeline, which must find it while scrambled versions of it come up empty. Each release shows whether it has passed. The free trial needs no exchange account, because Construct and Paper Books work on public data. The work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
