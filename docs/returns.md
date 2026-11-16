# Returns

This page is the devil's advocate on return and Sharpe. It is not a backtest. The process has not been backtested. No Sharpe below is a result for this desk.

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

## Claim

A 15% a year claim (plan) is not supported. The process has not been backtested.
