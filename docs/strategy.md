# Strategy

The strategy is the written run. There is no implementation. This page says which nodes own the decision, which nodes are only sentences, and how that run compares with the other strategies already in the record. It is a plan. It is not a backtest. No return, hit rate, or Sharpe on this page is a result.

This flow is better only as a drawback control, and only where the files already state the control. As a money-making system it is not better. No file in this repo shows a higher return for this run or for any alternative below. No return improvement survived the critique. The written run is unchanged. A new sleeve or a new model is not a higher return.

Where this page and [execution.md](execution.md), [nodes.md](nodes.md), [data.md](data.md), [testing.md](testing.md), or [returns.md](returns.md) differ, those pages are the spec. This page does not add a node. [returns.md](returns.md) owns the 15% answer. This page does not soften it.

Tags match the other pages. `(plan)` is the written plan. `(assumption)` is a planning assumption, not a fitted result. `(checked)` points at a source already checked in [data.md](data.md). A sentence that starts with `Inference:` is a reading. It is not a new rule.

## Where the strategy sits

The run is the chart and the steps in [execution.md](execution.md). [nodes.md](nodes.md) says who owns each number and what that node must not do. Code owns the topic, every figure, and every rank (plan). The small stats model owns the sector label (plan). A language model extracts a primary document into a schema and writes sentences that cite table figures (plan). It does not emit a return, a rank, or a topic score (plan).

The research decision is a signed expected excess return versus the local index over the next 1 to 4 weeks, shrunk hard toward zero, then a rank inside scored sectors (plan). The publish gate owns whether that excess is a view (plan). The episode count in this repo is unknown, and an unknown count fails the gate (plan). The decision this repo can describe is the evidence table, the words `no view`, and empty lists (plan). The center of the excess is zero until a walk-forward exists. No walk-forward has been run. The note is not safe to trade.

### Nodes that own the decision

These nodes choose the study, the label, the lists, or whether a view exists. A language model does not own any of them (plan).

| Node | Decision it owns | Who owns it |
| --- | --- | --- |
| Session calendar | Whether a new topic may open. One live sign. A `no view` note does not open a sign (plan). | Code |
| Required-rows gate | Stop, or continue to the topic score. The predicate is unlisted (plan). | Code |
| Topic score | One study. The four feeds are not blended (plan). | Code |
| Primary-row gate | Stop, or continue to the sector model (plan). | Code |
| Sector model | The signed expected excess for each touched sector in each market, or no score (plan). | Small stats model |
| Stock rank | The best list and the worst list. The cap is 0 until the publish gate has a record, then 3 names per market (plan). | Code |
| Publish gate | Stays shut for that market and topic type with fewer than 30 non-overlapping resolved walk-forward episodes, or when the shrunk score sits inside half that cell's trailing residual error (assumption). A shut gate is `no view` and empty lists. An unknown count stays shut (plan). | Code |
| Risk gate | `PASS` or `BLOCK` (plan). | Code |
| One repair | The route. A bad figure returns to the sector model. A bad sentence returns to the narrator. The topic stays (plan). | Code |

The sector model is ridge regression, or a monotonic scorecard if the sample is too short to fit (plan). The features are lagged residual flow, own-sector momentum, macro surprise, and same-market earnings surprise (plan). The fit is walk-forward only (plan). A deep net on daily prices is out (plan). The rank key is sector alignment plus one same-market fundamental (plan). The 20-session relative return is shown and is not a rank key (plan). There is no composite score (plan).

### Nodes that are only sentences

These nodes run only after the publish gate is open (plan). They do not own a number.

| Node | What it writes | What it does not own |
| --- | --- | --- |
| Bull | One sentence, citing a row, on what would confirm the sector label (plan). | The label, the rank, the topic |
| Bear | One sentence, citing a row, on what would invalidate the sector label (plan). | The label, the rank, a short |
| Narrator | The dashboard sentences from the table and those two sentences (plan). | Every figure, the lists, the topic |

Bull and bear each speak once. They do not see each other's draft. There is no second round (plan). The narrator cannot add a name and does not write numbers (plan).

### Nodes that are neither the decision nor only sentences

- Parallel ingest, the lagged flow residual, price and volume, and the evidence table write figures. Code owns them (plan). They do not choose the topic.
- Primary extract and filing extract fill a schema. Code owns the baseline and the surprise (plan). The language model does not own the decision.
- The checker recomputes every cited number. A separate language model checks entailment against the table (plan). Neither job emits a score. A repair does not refit (plan).
- The walk-forward line is code. This repo's output is the words `no track record` (plan).
- Insufficient data, `no view`, a blocked note, a failed note, and a published note end the run. The published note adds no new number (plan). No node places an order (plan).

`Inference:` a reader can follow the strategy on the code path from the session calendar through the publish gate. The sentence path does not choose it. While the gate is shut, the sentence path does not run.

## What the git record says

This page starts from `50442f8f0aa3c8c878507e942028061523031de2` on `master`. The message is `Answer the 15% question and close the named silences.` The body says the docs do not say the annual return will be larger than 15%, and that no backtest is added.

The history on that tip has four commits.

- `f7a3c420e27c8d01f9bdd289db77135138b9bdb0` is `Initial commit`. The tree is `.gitignore` and a `README.md` whose only line is `# Trading`.
- `91131d9a040f714f51b04e14981823e9c9e143a1` adds the run, the data page, the testing contract, and the case against a 15% a year target. The message says they do not report a backtest.
- `a3aeae4429212de43d0a35f378b98f1dfcecd973` adds the node page. The message says no backtest is added.
- `50442f8f0aa3c8c878507e942028061523031de2` is the tip this page starts from.

The tree on that tip is `README.md`, `.gitignore`, and `docs/data.md`, `docs/execution.md`, `docs/nodes.md`, `docs/returns.md`, and `docs/testing.md`. None of those files is an implementation. No commit on that tip adds a backtest, a hit rate, or a Sharpe.

## How every alternative is compared

Each alternative below is compared on the same five axes. No row has a measured return.

- **Who owns the number.** Who may emit the topic, the excess, the rank, or a grade.
- **Horizon.** The clock that decision is about. This repo states its own horizon. It does not invent a horizon the files do not record.
- **Look-ahead.** What a file in this repo says about future information. If no file here audits the other design, the cell says so.
- **What a trader can do with the output.** The action the output supports. This repo's note is not safe to trade.
- **A higher return in this repo.** A measured excess in a file here. A target, a class-range assumption, and a recorded reading of another repository are not that.

The four named designs are a recorded reading. Their files are not in this repo. This page does not use a star count. It does not treat a star count as a fact. It does not import a return from those designs.

## This written run

- **Who owns the number.** Code owns the topic, every figure, and the rank. The small stats model owns the sector label. The language model fills schema fields from a primary document and writes sentences. Code owns the baseline and the surprise (plan). The language model is banned from the topic score, the sector number, the rank, the risk gate, and the publish gate (plan).
- **Horizon.** The next 1 to 4 weeks (plan). The label starts at the next bar of the same market (plan). The decision close is that market's own session close (plan).
- **Look-ahead.** [testing.md](testing.md) is the contract: freeze the rules first, point-in-time membership, filing timestamps, flow vintage, a trailing beta that ends before the decision, purged overlapping labels, a refit per market and topic type, and a fill at the next bar. No test has been run. The beta-window length stays unpublished. The required-rows predicate stays unlisted. Filling either in on a seen path is a new test (plan).
- **What a trader can do.** Read the evidence. While the gate is shut, read `no view` and two empty lists (plan). The trader cannot send an order, size a book, or book `no view` as a flat. The note is not safe to trade.
- **A higher return in this repo.** No file shows one. [README.md](../README.md) says no return in this repo is a result. [testing.md](testing.md) says no return, hit rate, or Sharpe in this repo is a result.

## day-trader-skill

Recorded reading of Jakeschincariol/day-trader-skill. The design hands a file to the next step. Code does a `PASS`/`BLOCK` check. A replay runs before a ticket. A human says yes. Paper is the default. This desk's recorded take was the handoff, the code gate, and the replay. The files now hold those as schemas, the risk gate, and the walk-forward line. The recorded leave is the clock and the ticket: opening-range bars, a session path sim, and a broker ticket. This graph has no human-yes node. The default graph has no paper book (plan). The sleeve in [returns.md](returns.md) is a separate page.

- **Who owns the number.** In the recorded reading, code owns the check, and a human owns the yes. In this repo, code owns the risk gate. No human-yes node owns a number, because the node is not on the graph.
- **Horizon.** This repo's horizon is 1 to 4 weeks (plan). Opening-range bars and a session path sim are a session clock. They were left. The replay in this repo is a walk-forward hit rate of this scorecard, or the words `no track record` (plan). It is not a Monte Carlo of intraday bars (plan).
- **Look-ahead.** No file in this repo audits that design. This repo's own contract is [testing.md](testing.md), and it has not been run.
- **What a trader can do.** In the recorded reading, a trader can say yes on a paper default, and a broker ticket exists to be left behind. On this graph the trader can read a note. The trader cannot approve a ticket. No node places an order (plan).
- **A higher return in this repo.** No file shows one. The recorded reading does not become a result by being named here.

## TradingAgents

Recorded reading of TauricResearch/TradingAgents. Parallel analysts work, then a bull and bear debate, a risk debate, and a language-model portfolio manager. Later releases added point-in-time fixes. The recorded leave is a multi-round debate, and MACD or RSI as a 1 to 4 week model. The files keep parallel workers that write rows and do not write the score (plan). Bull and bear speak once, after the gate, and only by citing a row (plan). The risk gate is code, not a debate (plan). There is no language-model portfolio manager (plan).

- **Who owns the number.** In the recorded reading, the language-model portfolio manager owns the decision after the debates. In this repo, that manager is not a node. Code and the small stats model own the number. The recorded reading says the debate shares one prose state, so the speakers can talk a number into existence. This repo's ban is one turn, blind to the other draft (plan).
- **Horizon.** This repo does not record that design's holding period. It records the leave: MACD and RSI are not the 1 to 4 week model. This repo's model is the shrunk ridge or the monotonic scorecard (plan). A deep net on daily prices is out (plan).
- **Look-ahead.** The recorded reading says later releases added point-in-time fixes. [testing.md](testing.md) is the contract that keeps that lesson: membership, timestamps, vintages, a beta that ends before the decision, and a fill at the next bar. This repo does not contain those releases. No test has been run. A written contract is not a measured edge.
- **What a trader can do.** In the recorded reading, a trader can read a portfolio decision the model wrote. On this graph the trader can read evidence, or a note whose label was computed upstream. The trader cannot read a model portfolio. Forwarding the note to an execution desk is a misuse of the nodes (plan, and the node page).
- **A higher return in this repo.** No file shows one.

## daily_stock_analysis

Recorded reading of ZhuLinsen/daily_stock_analysis. The design has a calendar, source fallbacks, and a decision dashboard. The recorded leave is a language-model buy, watch, or sell grade. The files keep a session calendar and a dashboard whose label was computed upstream (plan). They do not keep a grade. The narrator does not write numbers (plan).

Source fallbacks are the piece the files only partly echo. If southbound is stale, HKEX turnover concentration is the flow fallback, and it is residualized the same way (plan). If the flow print the topic needs is missing, or the primary document is missing, or prices for the scored sector are missing, the run ends as insufficient data (plan). It does not publish a thinner thesis (plan). A chain of fallbacks that keeps a short file alive is not this run.

- **Who owns the number.** In the recorded reading, the language model owns a buy, watch, or sell grade on the dashboard. In this repo, code writes `no view` when the gate is shut, and the small stats model owns the label when a view exists (plan). The grade was left. That leave is the ban on a language-model rank (plan).
- **Horizon.** This repo does not record that design's holding period. This repo's horizon is 1 to 4 weeks (plan). The calendar in this repo names the Hong Kong session and the US session. It does not invent a bar on a holiday (plan).
- **Look-ahead.** No file in this repo audits that design. This repo's contract is [testing.md](testing.md), unrun.
- **What a trader can do.** In the recorded reading, a trader can read a grade. On this graph, while the gate is shut, the trader can read the evidence, the words `no view`, and empty lists (plan). The trader cannot obey a grade this desk does not print.
- **A higher return in this repo.** No file shows one. A grade is not a file here, and it would be the language-model rank the spec bans (plan).

## ai-hedge-fund

Recorded reading of virattt/ai-hedge-fund. Analyst signals share a schema. A code risk manager runs. Then a language-model portfolio manager and investor personas run. The recorded leave is the personas and the language-model portfolio manager. The files keep the schema at every boundary and a code risk gate (plan). They do not keep the personas or a model portfolio manager. The risk gate is not a panel of risk personalities (plan).

The recorded reading says the personas are one model wearing several hats, so the vote is correlated error. This repo has no such vote. That sentence is the recorded reason for the leave. It is not a measured correlation in this repo.

- **Who owns the number.** In the recorded reading, code owns the risk check and the language model owns the portfolio. In this repo, code owns the risk gate, and no language model owns a book. The gate checks the liquidity floor, same-market peers, a filled transmission slot, and fresh data (plan). A `PASS` does not mean the excess is different from zero.
- **Horizon.** This repo does not record that design's holding period. This repo's horizon is 1 to 4 weeks (plan). Expected excess is a research label, not a position size (plan).
- **Look-ahead.** No file in this repo audits that design. This repo's contract is [testing.md](testing.md), unrun.
- **What a trader can do.** In the recorded reading, a trader can read a size the portfolio manager wrote. On this graph the name cap is 0 until a record exists, and the note never names a short (plan). The trader cannot read a size. The MVP does not size a portfolio (plan).
- **A higher return in this repo.** No file shows one.

## Alternatives already rejected, and the two baselines

These are already in [returns.md](returns.md) and [testing.md](testing.md). They are compared on the same axes. None is a new candidate yet. The candidates that try to reopen them are below.

### Concentration

The name cap is 0 until the publish gate has a record, then 3 names per market (plan). The note never names a short (plan). Three names are a concentrated book. The class range is sector excess versus the local index, with the mass near zero (assumption). It is not a measured return on a three-name book. There is no tested path from the cap of 3 to 15% a year (plan).

- **Who owns the number.** Code owns the rank, inside the cap (plan). A language model cannot add a name (plan).
- **Horizon.** 1 to 4 weeks (plan).
- **Look-ahead.** Concentration has not been measured. Gap risk, crowding, borrow, and Hong Kong short-sale rules are out of scope (plan).
- **What a trader can do.** After a record, read at most three names a market, with no short and no size (plan). Until then, read empty lists. The trader cannot hold the cap as a book. This graph places no orders (plan).
- **A higher return in this repo.** No. Concentration fails this sample because the sample never measured it (plan, and [returns.md](returns.md)).

### Leverage

Leverage is not in the graph (plan). The MVP places no orders (plan). The gap from the assumed top of the class range, about 4% a year of sector excess, to the 15% target divides to 3.75 on those approximate inputs (arithmetic in [returns.md](returns.md)). The multiple is not a tested lever. The mass of the range is near zero (assumption). Leverage on a mass near zero scales noise, including the loss end of the range.

- **Who owns the number.** Nobody. There is no leverage node.
- **Horizon.** None in the graph. The label horizon stays 1 to 4 weeks (plan).
- **Look-ahead.** Not a test. A score inside half the trailing residual error is noise the publish gate drops (assumption). A lever on that noise is still noise.
- **What a trader can do.** Nothing this graph will send. Hong Kong stamp duty is 0.1% a side from 17 November 2023 (checked). A round trip is 0.2% (arithmetic). The yearly bill is unknown until turnover is frozen. The US commission is unknown. Leverage would multiply a bill this spec does not have a turnover for.
- **A higher return in this repo.** No. Leverage fails this sample ([returns.md](returns.md)).

### A different strategy

A different strategy could mean intraday trades, options, another market, or a language-model grade (plan). Those were left out of this MVP on purpose (plan). The opening-range clock, the session path sim, the broker ticket, the multi-round debate, MACD and RSI as the 1 to 4 week model, the language-model grade, the personas, and the language-model portfolio manager are that leave, as recorded above. The class range does not transfer to them (assumption). This repo has no record for them.

- **Who owns the number.** Not this graph. A language-model grade or a language-model portfolio manager would own it in prose. This repo bans that owner (plan).
- **Horizon.** Not the 1 to 4 week label, if the strategy is intraday. This page does not invent the other clock beyond the leave already named.
- **Look-ahead.** A different strategy leaves the sample. [testing.md](testing.md) does not transfer with it.
- **What a trader can do.** Not an action on this note.
- **A higher return in this repo.** No. A 15% a year claim from a different strategy is a new claim. It fails this sample because it leaves the sample ([returns.md](returns.md)).

### Treating 15% a year as an estimate

The user wants 15% a year (plan). That figure is a target. It is not an estimate from this sample. The claim is not supported. These pages do not say the annual return will be larger than 15%.

- **Who owns the number.** Nobody in this repo. A target is not a model output.
- **Horizon.** A year, set beside a 1 to 4 week research label (plan). The page does not convert one into the other.
- **Look-ahead.** There is no sample to leak. No walk-forward has been run.
- **What a trader can do.** Nothing. A trader cannot show the target beside the call. The call sits next to `no track record` (plan).
- **A higher return in this repo.** No. Treating the target as an estimate would invent one.

### Shrunk-to-zero

The published excess is zero unless the publish gate opens (plan). The model is already shrunk hard toward zero (plan). A score that does not beat zero excess, after the gate and after costs, is not a result ([testing.md](testing.md)). The comparison has not been run. There is no output yet.

- **Who owns the number.** The publish gate and the shrinkage. Both are code (plan).
- **Horizon.** The same 1 to 4 week label (plan).
- **Look-ahead.** The baseline is part of the unrun contract. It is not a result.
- **What a trader can do.** Read a published excess of zero while the gate is shut. That is `no view` (plan). It is not a flat the trader chose.
- **A higher return in this repo.** No output. This run has not been shown to beat zero.

### The sign of own-sector momentum

The sign of own-sector momentum over the same horizon is the second baseline (plan). Own-sector momentum is already a feature (plan). A flow residual that only restates that sign has not added a signal ([testing.md](testing.md)). The comparison has not been run. [testing.md](testing.md) says not to crown a winner in that document.

- **Who owns the number.** The sign of a feature the sector model already uses (plan). It is not a second model in the graph.
- **Horizon.** The same 1 to 4 week horizon (plan).
- **Look-ahead.** Unrun. The 20-session relative return is shown in the rank table and is not a rank key (plan). Using it as the key would leave the spec.
- **What a trader can do.** See the column. Sorting by it leaves the spec. The graph does not publish this sign as the note.
- **A higher return in this repo.** No output. The residual has not been shown to add a signal.

## Where the files say this flow is better

The files support a drawback control. They do not support a higher return. Each control below is a sentence already in the spec. The mapping to a named design is the recorded reading. `Inference:` the control is what this repo wrote instead of that design's decision owner. The inference is not a backtest.

- Code owns the topic, the figures, and the rank, and the language model is banned from those numbers (plan, [execution.md](execution.md)). `Inference:` that ban is the control against a debate, a buy/watch/sell grade, a persona vote, or a language-model portfolio manager owning the number.
- Bull and bear each speak once, cite a row, and do not see each other's draft (plan). There is no second round (plan). `Inference:` that is the control against a multi-round debate that can talk a number into existence.
- The risk gate is code, `PASS` or `BLOCK`, and it is not a panel of risk personalities (plan). `Inference:` that is the code check from the recorded reading of day-trader-skill and of ai-hedge-fund's risk manager, without a ticket and without personas.
- The replay is the walk-forward line of this scorecard, or `no track record` (plan). It is not a Monte Carlo of intraday bars (plan). `Inference:` that is the replay, on this repo's clock, without the session path sim.
- The dashboard shows a label that was computed upstream. The narrator does not write numbers (plan). `Inference:` that is the decision-dashboard shape without the language-model grade.
- Every boundary is a schema. A reason that does not contain a table figure fails closed (plan). `Inference:` that is the shared schema, without a language-model book on the other side of it.
- The publish gate sits in front of bull and bear. A shut gate prints the evidence, `no view`, and empty lists (plan). The repair cannot route around the gate (plan). One repair cannot re-pick the topic or refit (plan). Missing required data ends the run (plan). These are the controls against a thin thesis and against a second look. They are in [execution.md](execution.md).
- [testing.md](testing.md) freezes point-in-time membership, timestamps, vintages, and the next-bar fill. `Inference:` that is the point-in-time lesson from the recorded reading of later TradingAgents releases. The lesson is a leak control. No test has been run. A leak control is not a higher return.
- Raw flow does not enter the topic score or the sector model. The feature is the lagged residual (plan). `Inference:` that is the control against a print that restates the price. It is not an identified premium. The momentum-sign baseline is how the spec would notice a restatement. That comparison has no output.

## Where it is not better as a money-making system

No file in this repo shows a higher return. The prior review put this class at about -5% to +4% a year of sector excess versus the local index, with the mass near zero (assumption). That range is not a backtest of this repo. A result near the middle is about zero (assumption). A result at the top is about 4% a year of sector excess (assumption). 15% a year is a target (plan). It is not an estimate from this sample. The center of the excess is zero until a walk-forward exists. The note is not safe to trade.

The two baselines have no output. This flow has not beaten shrunk-to-zero. It has not beaten the sign of own-sector momentum. [testing.md](testing.md) refuses to crown a winner. Until that comparison exists, the center of the excess is the shrunk-to-zero line.

A trader can do less with this output than with the outputs in the recorded readings. A human yes and a paper ticket, a model portfolio, a buy/watch/sell grade, and a sized book are actions. This note's shut path is evidence, `no view`, and empty lists (plan). The files do not show that the refusal earns more money. They show that the refusal stops a false note. Stopping a false note is the drawback control. It is not a P&L.

The highest-return plan that survives [returns.md](returns.md) is still this graph, with the publish gate. Surviving means the plan does not pretend to have earned 15% a year (plan). It does not mean a measured edge. The process has not been backtested.

## Candidates a comparison invites

These are the return improvements a reader could try to pull out of the comparison. Each one is a proposal. None is a change. No file shows that any of them raises excess. The two voices below answer them. What survived is the section after the voices.

1. **Human yes, paper default, and a broker ticket.** Put them on this graph and call the paper path the return. The recorded reading of day-trader-skill has them. This graph does not.
2. **Multi-round debate, and MACD or RSI as the model.** Let bull, bear, and a risk panel revise the label, or replace the ridge with those indicators. The recorded leave of TradingAgents is those two pieces.
3. **Source fallbacks and a language-model grade.** Keep a short file alive and print buy, watch, or sell. The recorded leave of daily_stock_analysis is the grade. A thinner thesis is the hole this run already stops (plan).
4. **Personas and a language-model portfolio manager.** Size the names. The recorded leave of ai-hedge-fund is those two pieces. A size is a rank the language model is banned from, and it is a portfolio the MVP does not build (plan).
5. **Concentration, leverage, or 15% as an estimate.** Raise the cap above 3, scale the assumed top by the 3.75 multiple, or treat the target as a result. [returns.md](returns.md) already says each fails this sample.
6. **A new publish hurdle on the baselines.** Publish only when the scorecard beats shrunk-to-zero and the momentum sign. [testing.md](testing.md) already requires the comparison and forbids crowning a winner. There is no output. Writing the hurdle now would choose a rule on no path.
7. **Move the paper sleeve onto the default graph.** Call that sleeve the higher return. [returns.md](returns.md) already places the sleeve off the graph. It is one sector ETF against the local index ETF, flat at invalidation or at expiry, shut off after 500 basis points of drawdown from peak (plan). The numeric weekly loss limit is unknown until it is frozen. The sleeve states no Sharpe. It does not trade the best and worst lists. It does not convert the assumed range into 15% a year (plan).

## Devil's advocate

Two voices review the comparison and the seven candidates. They are written for this page. They are not quotations, and J.P. Morgan did not issue them. They are not rules. They do not add a node, a threshold, a vendor, or a backtest. They do not soften [returns.md](returns.md). They may say this flow is worse.

### A quantitative researcher

This flow is better as a written ban on who may emit a number. It is worse as a forecast. It is not a better money-making system. No file in this repo shows a higher return, so I will not rank these designs by a return. I will not say the annual return will be larger than 15%.

**This run.** The score is shrunk hard toward zero (plan). The published excess is zero unless the publish gate opens (plan). The episode count is unknown, so the gate is shut. The center of the excess is zero until a walk-forward exists. I have no hit rate and no Sharpe. The required-rows predicate is unlisted, and the beta-window length is unpublished. A gate I cannot replicate is not yet a control. I am not filling either blank in. An unlisted gate does not earn the target.

**day-trader-skill.** The recorded reading has a code check a machine can run, a human yes, and a replay before a ticket. This repo has the words of a gate and an unrun walk-forward line. I will not call the words a better control than an executable check I have not been shown. I also will not take opening-range bars, a session path sim, or a broker ticket onto a 1 to 4 week label. None of those clocks is a result in this repo. The human yes does not change the expectation of a shrunk score. It is a second owner. This sample does not measure that owner.

**TradingAgents.** Parallel rows are already this graph, and they do not own the score. A multi-round debate that shares a prose state can revise a label the small stats model already wrote. That is the drawback the one-turn ban controls. The ban is better control. It is not a better forecast. Later point-in-time fixes are the lesson [testing.md](testing.md) already writes. This repo has not run the lesson. MACD and RSI stay out. I have no holding period of theirs in these files, and I will not invent one to win the comparison.

**daily_stock_analysis.** A buy, watch, or sell grade is a language model owning the number. The ban is the right control, and the grade is not a premium. Source fallbacks that fill a hole are how a stop becomes a thinner thesis. A stop is not an episode. Manufacturing more labels from worse rows does not raise excess. The one fallback this spec already has, turnover concentration when southbound is stale, is residualized the same way. It is not a second source of return. I am not adding a chain of fallbacks.

**ai-hedge-fund.** A shared schema and a code risk check are already this graph. The personas, on the recorded reading, are one model in several hats. That vote is not a sample. The language-model portfolio manager is a rank and a size. Both are banned here, the rank by the language-model rule and the size by the MVP rule (plan). A `PASS` on this gate is a statement about a floor, a peer set, a slot, and a vintage. It is not a statement that the excess differs from zero. I will not take the personas or the manager back to manufacture a book.

**The rejected alternatives.** Concentration at three names, leverage, and a different strategy fail this sample for the reasons [returns.md](returns.md) gives. I will not raise the cap. I will not lever a mass near zero. The 3.75 multiple is arithmetic on an assumption, and the top of that assumption is about 4% a year of sector excess, not a forecast. Treating 15% as an estimate would turn a target into a result this sample does not contain.

**The baselines.** Shrunk-to-zero is the center. The sign of own-sector momentum has not been compared. A residual that only restates that sign has not added a signal. That sentence is already the testing page. This flow has not been shown to beat either baseline. That is the sense in which I will call it worse. I do not have a measured loss, and I will not invent one.

**The candidates.** None survives.

A human yes and a paper ticket do not change the shrunk excess. The ticket is an order node. I am not adding one. The paper default in that recorded reading is a ticket path. This repo's sleeve is a different page, already off the graph, and it does not convert the assumed range into the target. Neither one raises a return in a file here.

A multi-round debate revises the label in prose. MACD and RSI replace the model with the indicators the leave already rejected. Both are a different owner or a different strategy. They leave the sample.

Fallbacks plus a grade add episodes I would not count and a rank the language model may not emit. A stop written into a label is the selection the node page already refuses to call a measured bias.

Personas and a language-model portfolio manager are an LLM rank and a size. The cap stays 0 until a record exists, then 3. I am not raising it, and I am not handing the list to a model.

Concentration, leverage, and the target-as-estimate are already dead on the returns page. Restating them in a comparison does not revive them.

A hurdle that publishes only after both baselines lose is a knob. The testing page says the episodes the note reports are not the episodes that choose the rule, and it says not to crown a winner. There is no output to crown. I am not writing the hurdle.

Moving the sleeve onto the default graph does not create a Sharpe. The spec states none. I will not pretend the sleeve raises the return.

No candidate survives. I am not adding a sleeve or a model and calling it an improvement. The written run stays the written run. The flow is a drawback control with an unfinished predicate and an unrun test. It is not a return engine.

### A trader

This flow is worse for a trader. I cannot do anything with it by the close. The recorded readings hand me a yes, a grade, or a size. This note hands me evidence, the words `no view`, and empty lists. I will not say those other actions earn 15% a year. None of those earnings is a file here. I will not say this desk's annual return will be larger than 15%. The note is not safe to trade. I am not asking for an order node.

**This run.** I get no level, no stop, and no size. The two markets do not share a close. The decision close tells me which bar I am not allowed to fill. It does not hand me a ticket. I cannot book `no view` as a flat. The desk did not say flat. It said nothing. Empty lists are not a return.

**day-trader-skill.** On that recorded reading I can say yes, paper is the default, and a ticket exists. I can do more with that output. This desk left the ticket, and it has no human-yes node. Opening-range bars and a session path sim are the wrong clock for the 1 to 4 week note, and they are still a clock a desk can run. This calendar is not a book. I want the missing clock as a trader. I do not get to call it a higher return. A paper ticket on a mass near zero is still not 15% a year. I am not putting the ticket back.

**TradingAgents.** A portfolio decision is something a desk will forward. Forwarding this note is a misuse. A second round of debate is where I would ask for a level. This spec ends at one sentence, with no price and no size. I cannot trade the sentence. Point-in-time fixes do not give me a fill. The fill rule here is the next bar, and there is still no order. I will not call the debate a better year.

**daily_stock_analysis.** A buy, watch, or sell grade is a word I have seen people obey. This desk leaves the grade, and that is the control. It is also why the page is useless to me. On a short file their fallbacks would still print. This desk stops. I would rather have the note on that morning. The note would be the thinner thesis the spec refuses. I will not pretend the grade is a profit, and I will not add the fallbacks to feel less silent.

**ai-hedge-fund.** A size is what I opened the rank to find. The cap is 0 until a record exists. After that it is 3 names, no short, and still no size. Personas do not get me a locate. Borrow, Hong Kong short-sale rules, and the gap are out of scope, so a `PASS` is not permission to send. I am not taking the personas. I am not taking a language-model book. A sized story is more dangerous than an empty list, and the empty list is worse as a tool. Neither is 15%.

**The rejected alternatives.** Three names are still no size and no short. I leave with no hedge. Leverage multiplies a book this graph does not have, and it multiplies Hong Kong stamp duty. The rate is 0.1% a side from 17 November 2023 (checked). A round trip is 0.2% (arithmetic). The yearly bill is unknown. The US commission is unknown. I will not invent one. A different strategy is a different job. The target is a figure I cannot put in front of a risk committee. The line beside the call says there is no track record.

**The baselines.** Shrunk-to-zero is the note I will actually receive, and it pays nothing. The momentum sign is the column the page lets my eye sort. If I sort by it, I have left the spec. Neither baseline is a P&L in this repo. I cannot tell a committee that we beat them.

**The candidates.** None survives as a return, and none survives as something I can trade inside the rules I was given.

A human yes without a ticket is a meeting. The ticket is an order. I was not given an order node, and I am not adding one to dress up a zero.

A longer debate will not write a size. MACD and RSI will not become a 1 to 4 week book in these files. I am not swapping the model for them.

A grade gives me a word I could misuse. Fallbacks give me a note on a hole. I want both on a busy morning. They do not survive. The grade is the banned rank. The hole is the stop.

Personas and a language-model portfolio manager give me a size the returns page does not support. I would use the size. Using it is the failure. The cap stays where the spec put it.

Raising the cap, levering the assumed top, or reading 15% as an estimate is how a silent book becomes a loud target. I will not do it. The mass near zero, levered, is a louder zero, including the loss end of the assumed range.

A filter on baselines that have not been computed does not give me a position this week. It gives me another shut gate.

The sleeve, moved onto this graph, is still a paper page with no Sharpe and no path to the target. I still cannot run it from this note. The weekly loss limit is unknown until it is frozen. I am not moving it and calling the move a raise.

No return improvement survives. This flow is the worse trading product. That verdict does not add an order, a size, a grade, or a ticket. The process has not been backtested. The note is not safe to trade.

## What survived

The critique that holds is a refusal. The seven candidates do not survive. The written run is unchanged.

No order node is added. Leverage is not added. The name cap stays 0 until a record exists, then 3 names per market. A deep net is not added. A language-model rank is not added. No return is claimed. No backtest, hit rate, or Sharpe is invented.

The predicate stays unlisted. The beta-window length stays unpublished. The baselines stay unrun. The sleeve stays off the default graph. It does not raise the return. A new model does not raise the return. There is no new sleeve and no new model on this page.

[returns.md](returns.md) stays the owner of the return answer. 15% a year is a target (plan). The class range is about -5% to +4% a year of sector excess versus the local index (assumption). The center of the excess is zero until a walk-forward exists. The note is not safe to trade. The highest-return plan that survives is still this graph, with the publish gate. Surviving means the plan does not pretend to have earned 15% a year (plan). It does not mean a measured edge.

## What the record does not answer

- A measured annual return, a hit rate, or a Sharpe, for this run or for any named design. None is in this repo.
- A star count, a clone of those four repositories, or a holding period this page refused to invent.
- Whether a later walk-forward beats shrunk-to-zero, beats the momentum sign, lands inside the assumed class range, or lands elsewhere. The range is not a promise (assumption).
- The beta-window length, the required-rows predicate, the frozen USD liquidity floor, the frozen 5% denominator, and the sleeve's numeric weekly loss limit.
- Whether a human yes, a grade, or a sized book would have made money outside this repository. The commits show this repository does not contain that test.

## Claim

The strategy sits in the written run. Code and the small stats model own the decision. Bull, bear, and the narrator are sentences. This flow is better only as the drawback control the files already state. As a money-making system it is not better. No file in this repo shows a higher return. No return improvement survived. A 15% a year claim (plan) is not supported. The process has not been backtested. These pages do not say the annual return will be larger than 15%.
