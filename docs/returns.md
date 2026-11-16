# Returns

This page is the devil's advocate on return and Sharpe. It is not a backtest. The process has not been backtested. No Sharpe below is a result for this desk.

## The answer

No. These pages do not say that this desk's annual return will be larger than 15%.

The figure 15% a year is a target (plan). It is not an estimate from this sample, and the claim is not supported. No is not a measured path to some other return. No test has been run. [testing.md](testing.md) says no return, hit rate, or Sharpe in this repo is a result. `91131d9a040f714f51b04e14981823e9c9e143a1` says the docs cover the case against a 15% a year target and do not report a backtest. `a3aeae4429212de43d0a35f378b98f1dfcecd973` says no backtest is added.

The class range below is an assumption. The center of the excess is zero until a walk-forward exists. No walk-forward has been run. Concentration, leverage, and a different strategy fail this sample. The note is not safe to trade. The argument is the rest of this page. The two comments answer the same question. They are not quotations, and J.P. Morgan did not issue them. They are not rules. They do not add a node, a threshold, a vendor, or a backtest.

## The target

The user wants 15% a year (plan). That figure is a target. It is not an estimate from this sample. That claim is not supported.

## The class range

The prior review put this class at about -5% to +4% a year of sector excess versus the local index (assumption). The mass sits near zero (assumption). Sector excess means the sector minus the local index over the 1 to 4 week horizon (plan).

That range is not a backtest of this repo. It is not a promise that a future run will land inside it. It is the assumption the advocate uses.

## What the target would require

A result near the middle of that range is about zero (assumption). A result at the top is about 4% a year of sector excess (assumption). The gap from that top to 15% a year (plan) is the target divided by that top. The quotient is 3.75 (arithmetic on the plan target and the assumed top). The inputs are approximate, so the multiple is approximate. It is not a tested lever.

Closing the gap inside this sample would take concentration, leverage, or a different strategy. Each fails this sample.

## Concentration

The name cap is 0 until the publish gate has a record (plan). After the gate, the cap is 3 names per market (plan). The note never names a short (plan).

Three names are a concentrated book. The class range is sector excess versus the local index, with the mass near zero (assumption). It is not a measured return on a three-name book. There is no tested path from the cap of 3 (plan) to 15% a year (plan).

Gap risk, crowding, borrow, and Hong Kong short-sale rules are out of scope for the MVP (plan). Concentration fails this sample because the sample never measured it, and the spec forbids it until a record exists.

## Leverage

Leverage is not in the graph (plan). The MVP places no orders (plan). The 3.75 multiple above is what it would take to scale the assumed top of the range to the target (arithmetic). The mass of the range is near zero (assumption). Leverage on a mass near zero does not produce 15% a year (plan). It scales noise, including the loss end of the range.

The publish gate drops a shrunk score that sits inside half the trailing residual error (assumption). A score inside that noise, levered, is still noise. Thirty episodes and that width are planning assumptions, not a fitted result.

Hong Kong stamp duty is 0.1% a side from 17 November 2023 (checked). A round trip is 0.2% (arithmetic on that checked rate). The yearly duty bill is unknown until turnover is frozen. Leverage multiplies the bill. Leverage fails this sample because the spec has no leverage node, and the assumed excess is small next to the error the gate treats as noise.

## A different strategy

A different strategy could mean intraday trades, options, another market, or a language-model grade (plan). Those were left out of this MVP on purpose (plan). The class range does not transfer to them (assumption). This repo has no record for them.

A 15% a year claim (plan) from a different strategy is a new claim. It is not evidence for this graph. It fails this sample because it leaves the sample.

## What still stands

The highest-return plan that survives this advocate is still this graph, with the publish gate. Surviving means the plan does not pretend to have earned 15% a year (plan). It does not mean a measured edge.

Only after the gate passes, a separate paper sleeve may hold one sector ETF against the local index ETF (plan). The sleeve is not on the default graph (plan). It is flat at invalidation or at expiry (plan). Its loss limit must sit outside ordinary weekly noise (plan). The numeric weekly limit is unknown until it is frozen before any sleeve test. The sleeve shuts off after 500 basis points of drawdown from peak (plan). It does not feed the next note (plan). It does not trade the best and worst lists (plan).

This spec states no Sharpe for that sleeve.

The sleeve stays inside the same class. It does not convert the assumed range into 15% a year (plan). It is a plan for a paper page. It is not a backtest.

## Sharpe marks

A live Sharpe above 0.5 (assumption) in this class needs a pre-registered record. A live Sharpe above 1.0 (assumption) should be treated as overfit until proven otherwise. Both marks are experience. Treat them as assumptions. They are not a forecast. They are not a backtest of this desk. This spec does not claim either mark.

## Comments

Two voices answer the question on this page: will the annual return be larger than 15%? They are comments on the design. They are not quotations, and J.P. Morgan did not issue them. They are not rules. They leave the conclusion above standing.

### A J.P. Morgan quantitative researcher

No. I will not say this desk's annual return will be larger than 15%.

The user wants 15% a year (plan). That figure is a target. It is not an estimate from this sample. The prior review put this class at about -5% to +4% a year of sector excess versus the local index, and the mass sits near zero (assumption). A result near the middle is about zero (assumption). A result at the top is about 4% a year of sector excess (assumption). The gap from that top to the target divides to 3.75 on those approximate inputs (arithmetic above). The multiple is not a tested lever. I will not turn the top of an assumption into a forecast, and I will not turn the refusal into a promise that a future year lands under 15%. No walk-forward exists. The center of the excess is zero until one does. The score is shrunk hard toward zero (plan). The published excess is zero unless the publish gate opens (plan). There is no hit rate and no Sharpe for this desk.

The decision close is the close of the daily bar in the market the label belongs to. That names the bar the label must not include. It does not create a premium. The beta-window length stays unpublished. I am not filling one in. A length chosen after a path is seen is a new test. The required-rows predicate stays unlisted. I am not filling that list in. A gate I cannot replicate is not yet a control, and an unlisted gate does not earn 15% a year.

The repair restates the figure the checker recomputed and does not refit. That closes a second look at the same label. It does not add an edge. A stop is not an episode, because the sector model wrote no label. A published note, a `no view`, a blocked note, and a failed note do not erase a label. The weeks inside the noise stay in the cell. The stop count sits beside the 30 and does not increment it. I have no episode count. Unknown still fails the gate. Thirty was only ever enough for a sign (assumption).

Concentration at three names, leverage, and a different strategy fail this sample for the reasons above. Leverage on a mass near zero scales noise, including the loss end of the assumed range. I have no Sharpe to put on the sleeve, and the spec states none. Nothing in the files says the annual return will be larger than 15%.

### A J.P. Morgan trader

No. I will not say this desk's annual return will be larger than 15%. The note is not safe to trade. I am not asking for an order node.

The MVP places no orders (plan). The name cap is 0 until a record exists (plan). The episode count in this repo is unknown, and unknown fails the gate, so the note this repo can describe is evidence, the words `no view`, and empty lists (plan). I cannot book `no view` as a return. Empty lists are not 15% a year.

Hong Kong and the US do not share a close. The decision close is the close of the daily bar in the market the label belongs to. I cannot use the other market's close, and a holiday does not borrow one. That tells me which bar I am not allowed to fill. It does not hand me a level, a stop, or a size. The beta-window length stays unpublished. I cannot hedge a residual whose window has no public length, and I am not publishing a length to make the row tradable. The required-rows predicate stays unlisted. On a short file the desk stops. I cannot fill the hole with a broker quote and continue.

A stop does not count as an episode, and it does not tell me to hold, cut, or stay out. A blocked note, a failed note, a `no view`, and a published note still count when the sector model wrote an excess and that label has resolved. The published words `no view` are not the label. Counting them does not make them an order. The repair will not refit a model into a better story, and it will not change the topic. There is still no path from the repair to an order.

Hong Kong stamp duty is 0.1% a side from 17 November 2023 (checked). A round trip is 0.2% (arithmetic above). The yearly bill is unknown until turnover is frozen. The US commission is unknown. I will not invent one. Against an excess whose assumed mass is near zero, I do not have a net number, and I do not have a number larger than 15% a year.

The sleeve stays off the graph, states no Sharpe, and does not convert the assumed range into the target (plan). The highest-return plan that survives is still this graph, with the publish gate. Surviving means the plan does not pretend to have earned 15% a year (plan). It does not mean a measured edge. The process has not been backtested.

## What the record does not answer

- A measured annual return, a hit rate, or a Sharpe. None is in this repo. The two commits named above say the docs do not report a backtest.
- Whether a later walk-forward lands above 15%, inside the assumed class range, or elsewhere. The range is not a promise (assumption). No is not that forecast.
- The beta-window length. It stays unpublished.
- The required-rows predicate. It stays unlisted. The three ingest holes depend on a topic the gate has not scored.
- The frozen USD liquidity floor, the frozen 5% denominator, a live name count, the US commission, and the sleeve's numeric weekly loss limit.
- Whether a blocked note or a failed note opens a sign. A `no view` note does not (plan). That sign gap stays open. It is not the episode count.
- Whether a test was run outside this repository. The commits show this repository does not contain one.

## Claim

A 15% a year claim (plan) is not supported. The process has not been backtested. These pages do not say the annual return will be larger than 15%.
