# Train, test, held, reserve: why one hold-out is not enough once you have looked at it

_A hold-out judges a trading rule fairly only until you act on what it shows. Why history is better split four ways, with the last part opened once._

Anyone who tests a trading rule on past prices learns the first lesson quickly. A rule tuned on a stretch of history looks good on that stretch, because it was shaped to fit it. So you keep some history aside, tune on the rest, and check the rule on the part it never saw. That part is usually called a hold-out, or out-of-sample data.

It is a sound idea. It also wears out faster than most people expect, and it wears out through a perfectly reasonable habit: looking at the result and then doing something about it.

## How a hold-out gets used up

Take a made-up example. You search one stretch of history and come away with twenty candidate rules. You run all twenty on the hold-out. Most do poorly. Three do well. You keep the three and write down their hold-out scores as your evidence.

Those scores are no longer clean. The hold-out was supposed to judge the rules. Instead, it chose them. You kept those three because they scored well there, so of course they score well there.

Coins make it plain. Give twenty people a coin each and have them flip ten times. Keep the three with the most heads. Their sheets look impressive, and they would look just as impressive if every coin were fair, because you selected on the very thing you are now admiring. Ask the same three to flip again and they go back to being ordinary.

The same wearing-out also happens more quietly. The hold-out result disappoints, so you go back, change a setting and check again. A little better. You change another. Each round trip is a small choice made with the hold-out's help. After enough of them, the rule has been fitted to the hold-out as surely as it was fitted to the first stretch. It only took longer, and nothing dishonest happened at any step.

What comes out of this is a principle that is simple to say and hard to keep: the history that judges a rule must never be the history that chose it. The moment a stretch of history influences a choice, it has changed sides. It is now part of the choosing.

## Four parts instead of two

If looking and choosing use history up, the answer is to decide in advance which history may be used up, and to keep some back that is not used at all. One arrangement splits history four ways: train, test, held and reserve.

**Train** and **test** are the working parts. This is where rules are found, compared, adjusted and thrown out. You may look at these as often as you like. They are expected to wear out, and a good score here should impress nobody.

**Held** is history no choice was ever made on. The survivors of the first two parts are judged here. Because nothing was picked or tuned on it, a score on held means something that a score on the working parts cannot.

**Reserve** comes last of all. It exists because of the problem above. Once you have seen the held result, you are a person who has looked. You may be tempted to adjust something, or just to carry forward the survivors that did best on held, which is the twenty-coins mistake again. Reserve is the reading taken after all of that, on history still untouched.

## Keeping the last part honest

A four-way split only helps if it is kept. Three habits do most of the work.

Decide the split before you start, and write it down. Boundaries moved after seeing results are choices too.

Decide beforehand what a pass looks like. If a rule falls short on reserve, the honest result is that it fell short. The temptation will be to explain it away.

Look at reserve once. Look, adjust and look again, and you have turned it into one more working part. Then there is nothing left to judge with.

Even kept perfectly, the split has a limit. A rule that passes on every part has passed on the past. No arrangement of old prices can stand in for prices that have not happened yet. What the split does is narrower and still valuable: it stops a rule from being marked by the same history that picked it.

Ultimate Trading System, the software we build, splits history these four ways, train, test, held and reserve, so the history that judges a rule is never the history that chose it. Its Held and Reserve steps judge the survivors on history no choice was ever made on, held first and reserve last of all. The free trial needs no exchange account, because Construct and Paper Books work on public data. The work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
