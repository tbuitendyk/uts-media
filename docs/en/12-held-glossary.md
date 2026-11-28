# A word for testing a trading rule: held

_Held is the stretch of history that judges the rules a search kept, after they were chosen and before reserve. What it is, why test history is not enough, and how to use it._

Most people split history in two: one part to build a rule, one part to test it. The trouble starts the moment the test part is used to choose.

## What it means

Held is a stretch of history set aside for one job: judging the rules a search has already kept. It is not used to build a rule, and it is not used to choose between settings. It comes after train and test, and before reserve.

## Why it matters

Test history does real work while a rule is being made: it is where settings are compared and the better ones kept. That makes it part of the choosing. A rule that looks good on test history may only have been picked because it looked good there. Held is history the choices never touched, so a rule that holds up on it has shown something the choosing could not have given it.

## How to use it

Fix where held sits before you begin, next to the test part and apart from it. Make every choice on train and test. Then run the survivors once on held and see which still stand. Those that fail are dropped, not tuned on held: tuning on held turns it into a second test set. What survives goes on to reserve, the last stretch, opened once at the very end.

## Where it sits among the other checks

It is the third of the four parts of history: train, test, held, reserve. Before it come the planted pattern and how good "nothing" looks; with it, the simpler ways of trading the same stretch; after it, reserve and the greenlight.

## Where we use it

Ultimate Trading System, the software we build, splits history four ways in its sealed layout: train, test, held and reserve. A survivor faces held and, last of all, reserve, measured against four simpler ways of trading the same stretch. The history that judges a rule is never the history that chose it. There is no AI in what runs, and the same inputs give the same answer every time. The free trial needs no exchange account, and the work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

The word before this one, the greenlight: https://telegra.ph/A-word-for-testing-a-trading-rule-the-greenlight-11-27

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
