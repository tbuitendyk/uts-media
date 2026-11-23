# Paper trading is only a control if it runs on the same path as real orders

_A paper run is meant to show what a trading rule would have done with real money. It only can if the signals, orders, timing and costs take the same path. What breaks when they do not._

A trading rule has passed its backtest. Before money goes in, it is run forward on paper for a few weeks. If the paper results look like the backtest, the rule goes live. That is the plan most careful traders follow, and it is a good plan. But it rests on one assumption that is easy to break without noticing: that the paper run is doing the same thing the live run will do.

In the language of experiments, paper trading is a control. A control only works when it differs from the real thing in exactly one way. Here, the one difference should be that no money moves. Everything else, from the moment a price arrives to the moment a fill is recorded, should be the same.

## Where paper and live drift apart

Most paper setups are built separately from the live system, often quickly, and they differ in small ways that add up.

**The signal is computed differently.** The backtest code is reused for paper, but the live system has its own version written for speed. One rounds a value, one does not. One uses the bar's close, one uses the last trade a few seconds before it. Most days nobody notices. On the days that matter, the two disagree.

**The timing is different.** A paper run often decides on a finished bar and fills at that bar's price. A live run sees the bar finish, computes, sends an order, and waits. The price it gets is the price some seconds or minutes later. A rule that trades on short moves can lose most of its edge in that gap, and the paper run will never show it.

**The fills are imagined.** Paper fills are usually assumed: every order filled, in full, at the price asked. Real orders are partly filled, filled late, or not filled at all, and the ones that miss are often the ones that would have done best.

**The costs are left out or guessed.** Fees, spread and the cost of holding a position overnight are easy to leave out of a paper run, or to put in once as a round number and never check again.

**The failures never happen.** On paper there is no rejected order, no lost connection, no restart halfway through a trade. Live, there are. How the system behaves after each of those is part of what the rule will actually do with money, and paper built on a separate path never tests it.

Each of these on its own is small. Together they mean the paper run measures a slightly different rule from the one that will go live. When the two then disagree, nobody can say whether the rule changed or only the plumbing did.

## Making paper an honest control

The fix is plain to state: run paper and live through one path. The same code computes the signal. The same code builds the order. The same clock decides when. The same cost model is applied. At the very last step, one sends the order to a simulated book and the other to the exchange. That last step is the only difference, and so it is the only thing a gap between paper and live can be blamed on.

A few checks follow from that.

- Record what the paper run decided, when, and at what price, in the same form the live run records it. Then the two can be compared line by line, not only by their totals.
- Put costs in from the first day, at the level you expect to pay, and look at them again once real fills exist.
- Do not let paper be kinder than live. If live waits for the bar to close and then sends an order, paper should wait and price the same way.
- Treat a paper run that looks better than the backtest as a warning, not as good news. Usually it means something in the path is too easy.

None of this says the rule is good. A faithful paper run of a bad rule is still a bad rule. What it gives you is a reading you can trust: when paper and live are the same path, a difference between them is a difference in the market, not in your software.

This is how Paper Books works in Ultimate Trading System, the software we build: a rule that has passed its tests runs forward on paper, on the same path real money takes. Real orders start only when you switch them on, from a trading engine on a machine you choose. The free trial needs no exchange account, because Construct and Paper Books work on public data. The work runs on a machine of your own; nothing is hosted: https://ultimate-trading-system.com

This is software, not financial advice. Trading carries a substantial risk of loss, and passing these tests does not guarantee future results.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-en): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
