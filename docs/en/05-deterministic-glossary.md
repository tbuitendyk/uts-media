# A word for testing a trading rule: deterministic

_What it means for trading research to give the same answer for the same inputs, why it matters, and how to check your own tools._

One more word comes up whenever someone asks whether a trading rule is real: deterministic. Here it is in plain language.

## What it means

A test is deterministic when the same inputs give the same answer, every time. The same prices, the same settings and the same version of the tool produce the same trades, the same scores and the same verdict, whether you run it today or in six months, on your machine or on someone else's.

## Why it matters

A result you cannot reproduce is a result you cannot check. If two runs of the same test disagree, you no longer know whether a rule improved because of a change you made or because the tool simply answered differently this time. Every comparison in testing a rule, against a run with no information in it, against a simpler way of trading, against history the rule never saw, assumes that the only thing that changed is the thing you changed.

It also matters when someone else looks. A colleague, a reviewer or your future self should be able to take the same inputs and reach the same number. If they cannot, the number is a story, not evidence.

## What breaks it

Anything that answers differently from one call to the next: a service called from outside while the test runs, a setting that is not recorded with the result, history that is quietly revised, a step whose order is not fixed. None of these has to be large to make two runs disagree.

## How to check your own tools

Run the same test twice, with nothing changed, and compare the results line by line. Then ask whether each result says exactly which prices, which settings and which version produced it. If it does not, you cannot rerun it later even if the tool itself is deterministic.

## Where we use it

Ultimate Trading System, the software we build, is made this way. There is no AI anywhere in what runs: training, scoring, simulation and execution are plain arithmetic on market data, and the same inputs give the same answer every time. Every record set names the one it came from, so a result can be traced back to the prices and the settings that produced it, and worked out again. The free trial needs no exchange account, and the work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

The other four words, no-information run, held, reserve and planted pattern, are explained here: https://telegra.ph/Four-words-for-testing-a-trading-rule-no-information-run-held-reserve-planted-pattern-11-20

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
