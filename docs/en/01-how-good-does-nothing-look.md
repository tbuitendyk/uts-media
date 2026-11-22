# How good does "nothing" look? Why a backtest needs a no-information baseline

_A backtest score means little until you know what a rule with no information scores on the same history. How to build that baseline._

A backtest ends with a number. A rule was run over some years of past prices, and it came out ahead. The natural reaction is to be pleased. The more useful reaction is to ask a dull question: ahead of what?

Most people compare against zero. If the rule finished above where it started, it is called good. But zero is the wrong mark, and a few coins show why.

## A room full of coin flippers

Picture a hundred people in a room. Each flips a coin ten times and writes down the result. Nobody in the room has any skill at flipping coins. Even so, when the sheets are collected, a handful will almost certainly show eight heads or more. Sort the sheets from best to worst and the one on top looks like talent.

It is not talent. It is what the best of a hundred looks like when nothing is going on.

A search for a trading rule works the same way. You never test just one rule. You try a longer look-back and a shorter one, a tighter threshold and a looser one, this exit and that exit. Every combination is one more person in the room. Try a few thousand, and the best of them will show a handsome score on the history you searched, whether or not any of them knows a thing about prices.

So the number at the top of the list answers the wrong question. It says how the best of many tries scored. It does not say how much of that score the search would have produced anyway, with nothing behind it.

## Building "nothing" on purpose

The fix is to measure that directly. Before judging a rule, build a version of it that cannot possibly know anything, and put it through exactly the same process.

There are a few ordinary ways to do this. One is to replace the rule's signals with coin flips: the same number of entries, placed at random. Another is to keep the rule's own signals but shuffle them in time, so each one still exists but no longer sits beside the prices it was reacting to. A third is to shuffle the labels the rule was fitted to, so that whatever it learns, it learns from noise. The general idea has an ordinary name, a permutation test.

What these share is that the link between signal and price is cut on purpose, and everything else is left alone. Same history. Same costs. Same scoring. And, most important, the same search: if the real run tried a few thousand settings and kept the best, the no-information run tries a few thousand settings and keeps the best too.

Then you look at what "nothing" scored.

## What the baseline tells you, and what it does not

First, "nothing" is rarely zero. Imagine a made-up market that drifted upward for the whole stretch. Random buying ends ahead there. Imagine another that went sideways, with a cost on every trade. Almost everything ends behind. The baseline moves with the history, which is exactly why a fixed mark like zero misleads.

Second, one shuffle is not enough. A single no-information run can land high or low by luck, like a single flipper. Repeat it many times and you get a spread: where "nothing" usually lands, and how far it sometimes reaches. That spread is the real mark.

Third, it changes what counts as a result. A rule that sits inside the spread has shown nothing, however good its number looks alone. A rule that stands clear of the spread has earned a second look, and only that. It has passed one test on one stretch of history. The next step is history it has never seen.

A baseline does not tell you what a rule will do next. It removes one way of fooling yourself, which is mistaking the best of many tries for a discovery. That one is worth removing first, because it is easy to fall into and cheap to check. It also keeps effort honest: search harder and the real score climbs, but so does the score of "nothing". Watching the two rise together is a humbling and useful thing to see.

This is one of the things we built Ultimate Trading System to do without being asked. Each run is repeated with votes that carry no information, so the board shows how good "nothing" looks before anything is judged against it. A survivor then faces history it never saw, measured against four simpler ways of trading the same stretch. The free trial needs no exchange account, because Construct and Paper Books work on public data. The work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
