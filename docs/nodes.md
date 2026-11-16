# Nodes

This page walks every node in the chart in [execution.md](execution.md). It is a plan. It is not a backtest. No return, hit rate, or Sharpe on this page is a result.

The graph is a drawback control. The controls are the typed errors, the lagged residual, the two data gates, the language-model bans, the single repair, and the publish gate in front of bull and bear. They keep a language model from inventing a rank. The center of the excess is zero until a walk-forward exists. That reading sits on three lines already in this repo: the score is shrunk hard toward zero (plan), the published excess is zero unless the publish gate opens (plan), and no walk-forward has been run ([testing.md](testing.md)). The returns page puts the mass of this class near zero (assumption). None of those lines is a measured excess for this desk. The note is not safe to trade.

A 15% a year figure is a target (plan). It is not a result. The case against it stays in [returns.md](returns.md). This page does not soften that case.

Tags match the other pages. `(plan)` is the written plan. `(assumption)` is a planning assumption, not a fitted result. `(checked)` points at a source already checked in [data.md](data.md). A sentence that starts with `Inference:` is a reading. It is not a new rule. Where this page and [execution.md](execution.md), [data.md](data.md), [testing.md](testing.md), or [returns.md](returns.md) differ, those pages are the spec.

## What the git record says

`master`, as fetched for the page this edit started from, is `a3aeae4429212de43d0a35f378b98f1dfcecd973`. The history on that tip has three commits.

The root is `f7a3c420e27c8d01f9bdd289db77135138b9bdb0`. The message is `Initial commit`. The author is Kyle Au, dated Sun Oct 25 18:41:49 2026 +0800, and the committer is GitHub at the same time. The tree is `.gitignore` and a `README.md` whose only line is `# Trading`.

`91131d9a040f714f51b04e14981823e9c9e143a1` says `Add the Hong Kong and US research desk spec.` The body says the README maps one run and the MVP, the docs cover execution, data, look-ahead testing, and the case against a 15% a year target, and they do not report a backtest. Author and committer are Cursor Agent, Mon Nov 16 13:25:45 2026 +0000. The trailer is `Co-authored-by: kvgpt11 <kvgpt11@gmail.com>`. The diff expands `README.md` and adds `docs/data.md`, `docs/execution.md`, `docs/returns.md`, and `docs/testing.md`: 5 files changed, 505 insertions and 1 deletion.

`a3aeae4429212de43d0a35f378b98f1dfcecd973` says `Add the node-by-node strategy for the research desk.` The body says `docs/nodes.md` walks every node in the execution chart, including who owns each number and what the node must not do, the README links to it, and no backtest is added. Author and committer are Cursor Agent, Mon Nov 16 15:14:47 2026 +0000. The same co-author trailer is on the commit. The diff adds `docs/nodes.md` and one README link: 2 files changed, 778 insertions.

The files on that tip say the pages are a plan. `README.md` says no return in this repo is a result. [testing.md](testing.md) says no test has been run, and no return, hit rate, or Sharpe in this repo is a result. [returns.md](returns.md) on that tip says the process has not been backtested. The tip's message says no backtest is added. The answer on whether the annual return will be larger than 15% is the later edit of [returns.md](returns.md), not a sentence in these commits.

The remote ref `origin/cursor/hk-us-desk-docs-98cb` points at `91131d9a040f714f51b04e14981823e9c9e143a1`. It has no commit that `master` lacks. `master` has one commit that the ref lacks, the tip above.

## What the git record does not answer

- The git objects do not contain pull requests. A pull-request list for this repository, open and closed, was empty when this page was written, against `91131d9`. That list is not a git fact. It will go stale. This edit did not re-query that list. The sentence is about `91131d9`, not about the tip.
- The git record does not say why `cursor/hk-us-desk-docs-98cb` exists.
- The co-author trailer does not say what was reviewed, or that the text was accepted by anyone named in the parent commit.
- The commits do not record a live name count, a frozen USD liquidity floor, a frozen 5% denominator, a walk-forward episode count, a residual error, a hit rate, or a Sharpe. The docs mark those as a sketch, as unknown, as assumptions, or as unrun. The commits do not publish a beta-window length or a required-rows predicate. The docs leave the length unpublished and the predicate unlisted.
- The commits do not prove that no test was run outside this repository. They prove that this repository does not contain one. The files say no test has been run here.

## Locked rules

These rules bind every node. A node section below repeats the ones that node can break.

- Markets are Hong Kong (HKEX, HKD) and the US (NYSE and Nasdaq, USD) (plan). There are no A-shares (plan). China PMI can be a macro print because it hits Hong Kong (plan). That does not add a mainland market.
- The horizon is the next 1 to 4 weeks (plan).
- No node places an order (plan). The MVP does not size a portfolio and does not name a short (plan).
- Raw flow never enters the topic score or the sector model (plan). The feature is the lagged residual of flow on the same-window return (plan).
- Northbound is not a Hong Kong feature (plan). It does not fill the Hong Kong flow row and it does not fill the transmission slot (plan).
- The cross-market slot accepts revenue share or southbound holding (plan). Rate beta cannot fill the slot (plan). Southbound holding is not the daily buy and sell series (plan).
- The publish gate blocks bull and bear until that market and topic type have 30 non-overlapping resolved walk-forward episodes and the shrunk score sits outside half that cell's trailing residual error (assumption). Thirty and the width are planning assumptions, not a fitted result. The width is unknown until the episodes exist.
- The name cap is 0 until the publish gate has a record for that market and topic type, then 3 names per market (plan).
- The 20-session relative return is shown in the table and is not a rank key (plan).
- 15% a year is a target (plan). It is not a result. This repo states no hit rate and no Sharpe as a result. [returns.md](returns.md) says these pages do not say the annual return will be larger than 15%.
- The decision close is the close of the daily bar in the market the label belongs to (plan). The two session closes are not one decision.
- A repair restates the recomputed figure and does not refit (plan).
- A stop is not an episode (plan). A published note, a `no view`, a blocked note, and a failed note do not erase a label the sector model wrote (plan). The count is in [testing.md](testing.md).

The universe is Hang Seng, Hang Seng TECH, and S&P 500 (plan). The plan sketches that set at about 600 names (plan). That sketch is not a live count.

## Who owns a number

Code owns the topic, every figure, and every rank (plan). The small stats model owns the sector label: ridge regression, or a monotonic scorecard if the sample is too short to fit (plan). A language model extracts a primary document into the evidence schema, writes one bull sentence and one bear sentence after the publish gate is open, and narrates the dashboard (plan). It may label a headline or a filing into a sector from a fixed list (plan). A separate language model, in the checker, may test entailment against the table (plan). Neither job emits a score.

`Inference:` the session calendar, both gates, ingest, the evidence join, the rank, the walk-forward line, the risk gate, and the repair route are code because they are outside that closed list. The pages do not give those nodes a language-model job.

The language model is banned from the topic score, the sector number, the rank, the risk gate, and the publish gate (plan). It does not place an order, add a name, choose the topic, edit a score, or subtract in prose (plan).

| Node | Who owns the number | Run continues to |
| --- | --- | --- |
| Session calendar | Code | Parallel ingest |
| Parallel ingest | Code. No model | Required-rows gate |
| Required-rows gate | Code | Topic score, or the insufficient-data stop |
| Insufficient-data stop | Code. No thesis | End |
| Topic score | Code | The four evidence workers |
| Lagged flow residual | Code | Evidence table |
| Primary extract | Language model fills the schema. Code owns baseline and surprise | Evidence table |
| Filing extract | Language model fills the schema. Code owns baseline and surprise | Evidence table |
| Price and volume | Code | Evidence table |
| Evidence table | Code | Primary-row gate |
| Primary-row gate | Code | Sector model, or the insufficient-data stop |
| Sector model | Small stats model | Stock rank |
| Stock rank | Code | Publish gate |
| Publish gate | Code | No-view, or bull and bear |
| No-view | Code writes `no view` and empty lists | End |
| Bull | Language model, one sentence | Narrator |
| Bear | Language model, one sentence | Narrator |
| Narrator | Language model writes sentences. Code owns every figure on the page | Walk-forward base rate |
| Walk-forward base rate | Code | Risk gate |
| Risk gate | Code | Blocked note, or the checker |
| Blocked note | Code | End |
| Checker | Code recomputes. A separate language model checks entailment | Published note, one repair, or the failed note |
| Published note | No new number | End |
| Failed note | Code | End |
| One repair | Code chooses the return | Sector model, or the narrator |

## Session calendar

**Does.** The calendar names the Hong Kong session and the US session (plan). A holiday in one market does not invent a bar (plan). The next run marks the previous sign live, void, or expired before it opens a new topic (plan). A `no view` note does not open a sign (plan).

The decision close is the close of the daily bar in the market the label belongs to (plan). A Hong Kong label uses the Hong Kong session close. A US label uses the US session close. The two closes are not one decision. A holiday does not substitute the other market's close (plan). A print from the other market may be used only if it was public before this market's decision close (plan). The next bar is the next session of that same market (plan). The canonical clock is [execution.md](execution.md). The look-ahead check is [testing.md](testing.md).

Sign expiry, once a sign exists (plan):

- Macro and news expire after 5 sessions (plan).
- Flow expires after 10 sessions (plan).
- A filing expires at the next print or at 20 sessions, whichever is sooner (plan).

**Strategy.** One live sign at a time. The desk does not open a second topic on top of a sign that is still live, and it does not treat a holiday as a price. Expiry is written by topic type so a macro sign dies on a shorter clock than a filing. The testing page's purge of overlapping labels is a separate rule. This node does not compute that purge.

**Owner.** Code. A language model does not name the session, the holiday, or the expiry. See the inference under "Who owns a number."

**Inputs and outputs.** The node uses the Hong Kong session, the US session, and the previous sign if one exists (plan). A holiday in one market does not invent a bar (plan). Output is the session state and the mark on the previous sign: live, void, or expired (plan). A `no view` note does not open a sign, so that path has no sign to mark (plan). The spec does not list a schema for this node beyond those words.

**Must not.**

- Invent a bar on a holiday (plan).
- Substitute the other market's close, on a holiday or on a normal session (plan).
- Open a new topic while a previous sign is still live (plan).
- Open a sign from a `no view` note (plan).
- Treat 5, 10, or 20 sessions as a fitted half-life. They are written clocks (plan).
- Place an order.

The spec does not say whether a blocked note or a failed note opens a sign. It says a `no view` note does not (plan). That sign gap stays open on this page. It is not the episode rule.

## Parallel ingest

**Does.** Ingest calls four tool servers (plan). Each returns typed rows or a typed error (plan). They do not judge the topic (plan).

- Market data returns daily bars and dollar volume (plan).
- Flow returns southbound buy and sell, or HKEX turnover concentration if southbound is stale, plus US ETF flow and sector-fund flow (plan).
- Filings return HKEX announcements and SEC EDGAR filings on separate schemas (plan).
- The macro calendar returns the schedule, the consensus as of the prior session, and the actual only after it has printed (plan). The plan's set is CPI, payrolls, the Fed, PBoC and HKMA liquidity, and China PMI because it hits Hong Kong (plan).

Web fetch is an allowlist of primary hosts: the exchange, the central bank, the regulator, company IR, and EDGAR (plan). A recap domain is not a source (plan). The model calls a stats tool for every baseline (plan). It does not subtract in prose (plan). Tool retries sit inside a fetch. The cap is 3 (plan). They are not research iterations (plan).

Point-in-time membership for Hang Seng, Hang Seng TECH, and S&P 500 is required data ([data.md](data.md)). The execution chart names four servers, not a fifth. Hang Seng TECH launched on 27 July 2020 (checked). Rows before that launch are a back-cast from a vendor base date of 31 December 2014 (checked). They are not live membership.

**Strategy.** A missing print is a typed error, not a story the next node can smooth. Hong Kong filings and US filings stay on separate schemas so the join cannot pretend they are one form. Consensus is the prior session's consensus, so a live number that moved after the print cannot leak backward. The actual waits until it has printed. Retries are a fetch mechanic. They are not another pass at the thesis.

**Owner.** Code. No model judges the rows. The stats tool owns baselines. A language model does not own a figure here.

**Inputs and outputs.** Inputs are the four servers, the allowlisted fetch, and the membership tape the data page requires. Outputs are typed rows or typed errors, each print in its own currency (plan). The only conversion in the MVP is the liquidity floor, later, at 7.80 HKD per USD (plan). Flow rows carry a vintage (plan). Filing rows carry the HKEXnews release time or the EDGAR acceptance time (plan). A period-end date is not a timestamp (plan).

**Must not.**

- Judge the topic (plan).
- Use a recap domain as a source (plan).
- Fill a Hong Kong flow row with northbound (plan).
- Treat the two sides of 13 May 2024 and 19 August 2024 as one Stock Connect regime (checked dates; the split is in [testing.md](testing.md)). Northbound is still not a Hong Kong feature on either side (plan).
- Load the Hang Seng TECH back-cast as live membership or as a live sector return ([testing.md](testing.md)).
- Use a current constituent file as history ([testing.md](testing.md)).
- Use a free bar file adjusted as of today as a point-in-time tape ([data.md](data.md)).
- Subtract in prose (plan).
- Count a retry as a research iteration (plan).
- Place an order.

If the flow print the topic needs is missing, or the primary document is missing, or prices for the scored sector are missing, the run ends as insufficient data (plan). It does not publish a thinner thesis (plan). Those holes are enforced at the gates below. The prose names the topic, and the topic node has not run yet. See the required-rows gate.

## Required-rows gate

**Does.** The chart asks whether required rows are present. No goes to the insufficient-data stop. Yes goes to the topic score.

**Strategy.** The desk does not score a topic on a hole. A typed error is supposed to end the run rather than become a thinner thesis (plan).

**Owner.** Code. The predicate is a schema check. A language model does not waive a missing row.

**Inputs and outputs.** Input is the typed output of ingest. Output is yes or no.

`Inference:` the chart draws this gate before the topic, and the primary-row gate after the evidence join. The prose names three terminal holes, the flow print the topic needs, the primary document, and prices for the scored sector, and those holes depend on a topic this gate has not scored yet (plan). [execution.md](execution.md) leaves the predicate unlisted. [testing.md](testing.md) says filling it in from a seen path is a new test. This page does not invent the missing list.

**Must not.**

- Let a language model decide that a partial pull is enough (plan).
- Continue to the topic score on a no.
- Turn a typed error into a prose hedge.
- Place an order.

## Insufficient-data stop

**Does.** The run ends (plan). It does not publish a thinner thesis (plan). The chart reaches this node from the required-rows gate and from the primary-row gate. Missing data ends the run (plan).

**Strategy.** A hole is terminal. The desk prints nothing that a reader can mistake for a view with footnotes. This stop is distinct from `no view`, which still publishes the evidence, the words `no view`, and empty lists (plan).

**Owner.** Code. There is no number to own. A language model does not write a substitute thesis.

**Inputs and outputs.** Input is a no from either gate, or one of the three holes named under ingest (plan). Output is the end of the run. The spec does not define a published document for this stop.

**Must not.**

- Publish a thinner thesis (plan).
- Fill the hole with northbound, a recap, a live consensus, or a language-model story (plan).
- Open a path to bull, bear, the narrator, or the rank.
- Place an order.

The stop is not a walk-forward episode ([testing.md](testing.md)). The sector model wrote no label. The stop does not increment the 30. When the topic type and the market are already known, the stop is recorded on that cell. When they are not, it stands outside every cell. The spec does not say the stop opens a sign. That gap stays open. The comments name the selection that remains: the scored cell is the weeks the files were complete enough to label. They do not turn a stop into a label.

## Topic score

**Does.** Code scores four feeds and picks one study (plan). It does not blend them (plan).

- Capital flow.
- News that moves an index or a GICS sector.
- The next scheduled macro print.
- Filings.

The score is a robust z-score of each feed versus its own 20-session baseline, times breadth (plan). Surprise is the gap versus that baseline (plan). Breadth is how many sectors the item touches (plan). The tie-break is macro, then filings, then flow, then news (plan). News alone is the weakest topic (plan).

News is eligible from the last 5 sessions (plan). A filing topic sits inside a 10-session window (plan). The macro tool may nominate a print only when the consensus gap or the recent sector move clears the same z-score bar as the other feeds (plan). Otherwise the print is not a topic (plan).

Flow in the topic score is the lagged residual of flow on the same-window return (plan). Raw net buy does not enter the topic score (plan). Northbound is not a Hong Kong feature (plan). The Hong Kong flow feed is southbound, or HKEX turnover concentration when southbound is stale (plan). The fallback is residualized the same way (plan).

A language model may label a headline or a filing into a sector from a fixed list (plan). It may not choose the topic or edit the score (plan). Embeddings may dedupe near-copy headlines (plan). They are not a score (plan). High similarity between the thesis and secondary recaps is a reject, not support (plan).

**Strategy.** One study, so the note cannot average four stories into a smooth paragraph. The robust z-score puts each feed on its own 20-session baseline before breadth weights it. Macro has to clear the same bar as the other feeds, so a scheduled print is not a topic every week. The tie-break prefers macro, then filings, then flow, then news, when scores tie. Flow can win only as a residual after the same-window return, so raw buying pressure that restates the price does not choose the topic. Secondary copy that matches the thesis is a reason to reject, not a citation.

**Owner.** Code owns the score. The robust z-score is that code, not a fitted sector model and not a language model. A language model may apply a fixed sector label (plan). Embeddings may dedupe (plan). Neither owns the number.

**Inputs and outputs.** Inputs are the four feeds as typed rows, each feed's own 20-session baseline, and the fixed sector list. Output is one topic decision. The boundary is a schema (plan). The spec names the schema and does not list its fields beyond the choice of one feed and the score that chose it.

The spec does not define how an item "touches" a sector beyond the word breadth (plan). This page does not add a definition.

**Must not.**

- Blend the four feeds (plan).
- Let a language model choose the topic or edit the score (plan).
- Let raw net buy enter the score (plan).
- Let northbound enter as a Hong Kong feature (plan).
- Nominate a macro print that misses the same z-score bar (plan).
- Use embeddings as a score, or treat similarity to a recap as support (plan).
- Use news outside the last 5 sessions, or a filing topic outside the 10-session window (plan).
- Emit a return (plan).
- Place an order.

## Lagged flow residual

**Does.** This worker runs only for the chosen topic (plan). It writes the lagged residual (plan). It does not write the score (plan). The hedge beta is a trailing window that ends before the decision (plan). Raw net buy stops at the vintage and does not enter the table as a score ([data.md](data.md)).

The Hong Kong series is southbound day-end buy and sell, with HKEX turnover concentration as the fallback when southbound is stale (plan). The US series is ETF flow and sector-fund flow (plan). Both are residualized the same way (plan). Northbound does not fill the Hong Kong flow row (plan).

**Strategy.** Raw net buy can restate the same-window return. The control is to lag flow and residualize it on that return, with a beta estimated on a window that ends before the decision, so the label is not inside the hedge. The same residual rule already applied inside the topic score (plan). This node writes the row the evidence table will hold. It does not get a second vote on which topic won.

**Owner.** Code. The hedge beta is a trailing calculation inside that code. It is not the sector ridge, and a language model does not own it. The numbers worker sees rows, has no web fetch, and has no prose (plan).

**Inputs and outputs.** Inputs are the flow vintage and the same-window return. The beta window ends before the decision (plan). The length stays unpublished ([execution.md](execution.md) and [testing.md](testing.md)). This page does not set it. Output is an evidence row for the residual: figure, baseline, surprise, currency, and vintage (plan). Surprise is code (plan).

**Must not.**

- Pass raw net buy into the topic score or the sector model (plan).
- Use northbound as the Hong Kong series (plan).
- Swap southbound holding into this row. Holding is the transmission slot, not the daily buy and sell series ([data.md](data.md)).
- Include the label, or the decision, in the beta window (plan).
- Publish a window length, or choose one after seeing a path. The length stays unpublished. The testing page says filling it in on the reported path is a new test.
- Fetch the web or write prose (plan).
- Write the topic score (plan).
- Place an order.

## Primary extract

**Does.** Primary extract searches for the exchange notice, the central-bank text, or the company filing (plan). It fills the evidence schema (plan). It does not summarize the web (plan). It sees the document and the schema (plan). It does not see rank tools (plan).

**Strategy.** The thesis has to rest on a primary document. A recap is not a source (plan). The schema forces the extract into fields the checker can recompute. The language model does not get to turn the page into a story and call the story evidence.

**Owner.** The language model fills the schema from the document (plan). Code, through the stats tool, owns the baseline and the surprise (plan). The language model does not subtract in prose (plan). It does not own a return, a rank, or a topic score (plan).

**Inputs and outputs.** Inputs are the allowlisted document and the evidence schema. Outputs are schema fields: date, market, source URL or ticker, figure, unit and currency, baseline, surprise, and vintage timestamp (plan, and the row in [data.md](data.md)). The blanks in the data page are a target shape, not a sample.

**Must not.**

- Summarize the web (plan).
- Use a recap domain (plan).
- See rank tools (plan).
- Choose the topic or edit the score (plan).
- Subtract in prose (plan).
- Emit a return, a rank, or a topic score (plan).
- Place an order.

## Filing extract

**Does.** Filing extract reads filings only for names already on the sector shortlist (plan). Hong Kong reports and US filings stay on separate schemas (plan). It sees the document and the schema (plan). It does not see rank tools (plan). Timestamps are the HKEXnews release time and the EDGAR acceptance datetime (plan). A filing accepted after the decision is invisible ([testing.md](testing.md)).

**Strategy.** The worker reads filings only for names already on the sector shortlist, not the whole universe (plan). Separate schemas keep Hong Kong reports and US filings from being treated as one form with one calendar (plan). The peer set and the prior report are same-market later, at the rank (plan). This node supplies the rows. It does not make that comparison.

`Inference:` the rank has not run when this node runs. The shortlist is not the later best list or worst list. The spec does not define the shortlist beyond "names already on the sector shortlist" (plan). This page does not add a definition.

**Owner.** The language model fills the schema (plan). Code owns baseline and surprise (plan). The language model does not own a rank.

**Inputs and outputs.** Inputs are the filing, its release or acceptance time, the schema for that market, and the shortlist. Outputs are evidence rows on that market's schema. A headline about the filing is not a substitute for the timestamp ([testing.md](testing.md)).

**Must not.**

- Read the whole universe (plan).
- Merge Hong Kong and US filings onto one schema (plan).
- See rank tools (plan).
- Use a period-end date as the timestamp (plan).
- Use a filing accepted after the decision ([testing.md](testing.md)).
- Choose the topic, edit the score, or emit a rank (plan).
- Place an order.

## Price and volume

**Does.** Code writes the return, realized vol, and volume versus its 20-session median, on 60 sessions of daily bars, for the affected sector ETFs and the index (plan). The research window is 60 sessions (plan). Dollar volume feeds the liquidity floor later ([data.md](data.md)).

**Strategy.** The price reaction is a measured row. The window and the median are written, so the note cannot pick a lookback after it sees the move. These rows describe the sector ETF and the index. They are not the 1 to 4 week excess label. That label belongs to the sector model, and the testing page starts it at the next bar.

**Owner.** Code. The numbers worker has no web fetch and no prose (plan). A language model does not write the return. A deep net on daily prices is out (plan).

**Inputs and outputs.** Inputs are 60 sessions of daily bars for the affected sector ETFs and the index (plan). The data page also requires daily bars for universe names, because the rank's liquidity floor and the shown relative return need them ([data.md](data.md)). Outputs of this node, as the execution page draws it, are the return, realized vol, and volume versus its 20-session median (plan).

The 20-session relative return is shown at the stock rank and is not a rank key (plan). The spec does not say which node computes that column. This page does not assign it.

**Must not.**

- Use a deep net on daily prices (plan).
- Let a language model write the return, the vol, or the volume ratio (plan).
- Invent a bar on a holiday (plan).
- Treat a file adjusted as of today as point-in-time ([data.md](data.md)).
- Book a fill. The decision may use prints known by that session, and the measured label starts at the next bar ([testing.md](testing.md)). A fill on the decision bar is look-ahead ([testing.md](testing.md)).
- Turn this return into the rank key or the topic score (plan).
- Place an order.

## Evidence table

**Does.** The worker rows join into one evidence table (plan). The row carries date, market, source URL or ticker, figure, unit and currency, baseline, surprise, and a vintage timestamp (plan). Surprise is code (plan). A reason that does not contain a table figure fails closed (plan).

**Strategy.** Later sentences may cite this table and no other number. One join, with a vintage on every row, is what the checker recomputes against. Raw net buy stops at the vintage and does not enter the table as a score ([data.md](data.md)). The residual is the flow figure the score is allowed to use (plan).

**Owner.** Code joins the rows and owns every figure in them, including surprise (plan). A language model does not compute a column.

**Inputs and outputs.** Inputs are the lagged-residual row, the primary-extract row, the filing rows, the price and volume rows, the macro rows, and the universe filter from point-in-time membership ([data.md](data.md)). Output is one evidence table. Northbound does not appear as a Hong Kong feature row (plan).

**Must not.**

- Admit raw net buy as a score (plan).
- Admit northbound as a Hong Kong feature (plan).
- Let a language model write surprise in prose (plan).
- Publish a thesis when the primary row is missing. That is the next gate (plan).
- Drop the vintage. The checker needs it to recompute (plan).
- Place an order.

## Primary-row gate

**Does.** The chart asks whether the primary row is valid. No goes to the insufficient-data stop. Yes goes to the sector model. A missing primary row ends the run as insufficient data (plan).

**Strategy.** A thesis without the primary document is the hole the spec refuses to paper over (plan). The sector model does not run on recaps.

**Owner.** Code. A language model does not waive the row.

**Inputs and outputs.** Input is the evidence table. Output is yes or no. The chart says "valid" and the prose says "missing" (plan). The spec does not define valid beyond the primary row being present. This page does not add a definition.

**Must not.**

- Continue to the sector model on a no (plan).
- Accept a recap row as the primary row (plan).
- Let a language model declare the row valid.
- Place an order.

## Sector model

**Does.** For each touched GICS sector in each market, the model writes a signed expected excess return versus the local index over 1 to 4 weeks (plan). Sectors with no evidence stay unscored (plan). The model does not force a view on every sector (plan).

The MVP fit is ridge regression, or a monotonic scorecard if the sample is too short to fit (plan). The features are lagged residual flow, own-sector momentum, macro surprise, and same-market earnings surprise (plan). The score is shrunk hard toward zero (plan). The fit is walk-forward only (plan). A deep net on daily prices is out (plan).

Sector scores are per market (plan). A US pass with an empty Hong Kong transmission slot prints no Hong Kong names (plan). The slot accepts revenue share or southbound holding (plan). Each must be at least 5% of the relevant total (plan). That floor is frozen before any test (plan). The denominator is frozen with the floor (plan). It is unknown in this spec until that freeze. Rate beta cannot fill the slot (plan). An empty slot drops the link (plan).

**Strategy.** The research label is a shrunk, walk-forward, per-market excess versus the local index. Shrinkage is how the spec keeps the center on zero until a walk-forward says otherwise. No walk-forward has been run. A US result does not become a Hong Kong name list. The link exists only when revenue share or southbound holding clears a floor that has to be frozen, with its denominator, before any test. Rate beta is a common story for why the two markets moved together. It is not a legal filler for this slot.

Expected excess return is a research label (plan). It is not a position size. Crowding, borrow, Hong Kong short-sale rules, and gap risk are out of scope (plan).

**Owner.** The small stats model owns the sector number (plan). Code runs it. A language model is banned from the sector number (plan). It does not type the return.

**Inputs and outputs.** Inputs are the evidence table, restricted to sectors that have evidence, and the slot inputs when a cross-market link is claimed: revenue share or southbound holding, each against a frozen denominator (plan). Outputs are a signed expected excess per scored sector per market, or no score. The boundary is the sector-label schema (plan).

The fit has to obey [testing.md](testing.md). Each market is fit on its own, and each topic type is fit on its own (plan). A pooled model fails that step. Any beta ends before the decision (plan). Overlapping labels are purged before they count (assumption, and the testing page). The label horizon is 1 to 4 weeks (plan). The return starts at the next bar (plan).

**Must not.**

- Force a view on a sector with no evidence (plan).
- Pool markets, or copy a US coefficient onto Hong Kong flow (plan, and [testing.md](testing.md)).
- Fill the slot with rate beta, northbound, or an empty value (plan).
- Swap the daily southbound buy and sell series in for southbound holding ([data.md](data.md)).
- Use raw flow as a feature (plan).
- Use a deep net on daily prices (plan).
- Fit on a window that includes the label ([testing.md](testing.md)).
- Let a language model emit the sector number (plan).
- Treat the label as a position size or an order (plan).
- Claim the score is a measured excess. It is not. No test has been run.

A bad figure on the repair edge returns here (plan). The return restates the figure the checker recomputed (plan). It does not refit (plan). It does not change coefficients, the training window, the features, or the topic (plan). A refit after a failed check would be a second look, and [testing.md](testing.md) calls that repair a new test. A repair is not a second episode (plan).

## Stock rank

**Does.** Rank is code, inside scored sectors only (plan). The liquidity floor is a hard filter first (plan). Floors are compared in USD at 7.80 (plan). That rate is the frozen comparison constant, not a live FX print (plan). HKD 20 million at 7.80 is about USD 2.6 million (plan arithmetic). It is not the same bar as USD 20 million (plan). The USD level of the floor is unknown until it is frozen before any test (plan).

The rank key is sector alignment plus one same-market fundamental (plan). The fundamental is revenue surprise, EPS surprise, or net-debt direction, from the latest report (plan). The peer set and the prior report are same-market (plan). The 20-session relative return is shown in the table (plan). It is not a rank key (plan). There is no composite score (plan).

A name with earnings or a named macro print inside the horizon is dropped (plan). A name without a number is dropped (plan). The note never names a short (plan). The name cap is 0 until the publish gate has a record for that market and topic type (plan). If a sign is later allowed, the cap is 3 names per market (plan). The narrator cannot add a name (plan).

**Strategy.** The screen is not "what just moved." Liquidity is a hard filter before the names are ranked. The key is alignment with the sector label plus one fundamental from the same market's own reports. The 20-session relative return stays visible so a reader can see the move, and it stays out of the key so the sort cannot reward recency. Until this market and topic type have a publish-gate record, the cap is 0 and both lists are empty (plan). After that, the cap is 3 names per market, and the note still never names a short (plan).

**Owner.** Code (plan). A language model is banned from the rank (plan).

**Inputs and outputs.** Inputs are the scored sectors, dollar volume compared at 7.80, one same-market fundamental, point-in-time membership, and the earnings and macro prints inside the horizon. Output is a best list and a worst list, capped, or two empty lists while the cap is 0. The table shows the 20-session relative return (plan). The boundary is the name-rank schema (plan).

The chart draws this node on the way to the publish gate even when the gate will shut. A shut gate does not publish a rank or a name (plan). The cap of 0 and the shut gate are both in the spec. This page does not delete the node from the chart.

The spec states the rank key and states that there is no composite score (plan). It does not give weights. This page does not add weights.

**Must not.**

- Rank outside scored sectors (plan).
- Use the 20-session relative return as a rank key (plan).
- Build a composite score (plan).
- Compare peers or the prior report across markets (plan).
- Treat HKD 20 million as the same bar as USD 20 million (plan).
- Use 7.80 as a live FX print or as an FX trade (plan).
- Keep a name with earnings or a named macro print inside the horizon (plan).
- Keep a name without a number (plan).
- Name a short (plan).
- Emit more than the cap: 0, then 3 per market (plan).
- Let the narrator add a name (plan).
- Place an order, or size a position (plan).

## Publish gate

**Does.** The publish gate is code, applied per market and topic type (plan). A US flow record does not open a Hong Kong macro note (plan).

The gate stays shut in either case (assumption):

- Fewer than 30 non-overlapping resolved walk-forward episodes in that cell (assumption).
- A shrunk score inside half that cell's trailing residual error (assumption).

Thirty and the error width are planning assumptions. They are not a fitted result. An unknown episode count fails the gate (plan). An open episode is not resolved (plan). An overlapping label does not count (assumption). The plan treats 30 episodes as enough for a sign only (assumption). The plan sketches the hit-rate error at that count as about 9 points (assumption). That sketch is not the trailing residual error (plan). The residual error is unknown until the episodes exist (plan).

A shut gate publishes the evidence table, the words `no view`, and empty lists (plan). It does not publish a sector return, a rank, or a name (plan). Bull and bear do not run (plan). The repair edge cannot route around the gate (plan).

What counts is in [testing.md](testing.md), and the run states it again in [execution.md](execution.md). One decision in the cell is one episode once the label window has ended and it does not overlap the next decision. Several sectors do not multiply it. The label is the excess the sector model wrote, not the published words `no view`. A published note, a `no view`, a blocked note, and a failed note do not erase that excess. A cell the model left unscored does not count. A stop does not. The stop count is not a third hurdle.

**Strategy.** Bull and bear stay blocked until both hurdles clear. The hurdles are a count of non-overlapping resolved episodes in that same cell, and a shrunk score outside half the cell's own trailing residual error. Both numbers are assumptions. The gate is shut today, because the episode count is unknown and an unknown count fails (plan). The about-9-point sketch is a comment on a hit rate at that count. It is not the width the gate uses, and it is not a result.

The testing page freezes these thresholds before any outcome is computed. They are not knobs to search (assumption). The episodes the note reports are not the episodes that choose the rule ([testing.md](testing.md)).

**Owner.** Code (plan). A language model is banned from the publish gate (plan).

**Inputs and outputs.** Inputs are the cell (one market, one topic type), the count of non-overlapping resolved episodes in that cell, the shrunk sector score, and half the cell's trailing residual error. Output is open or shut. Unknown count is shut (plan). Unknown width cannot show that the score is outside it, so the second hurdle stays failed until the episodes exist. That is the spec's own statement that the width is unknown until then (plan).

**Must not.**

- Open on an unknown, overlapping, or unresolved count (plan, assumption).
- Treat 30, the half-width, or the about-9-point sketch as a fitted result (assumption).
- Use the about-9-point sketch as the trailing residual error (plan).
- Let a US cell open a Hong Kong cell, or any cell open a different topic type (plan).
- Publish a sector return, a rank, or a name when shut (plan).
- Run bull or bear when shut (plan).
- Let the repair skip the gate (plan).
- Drop a resolved label because the note was `no view`, blocked, or failed ([testing.md](testing.md)).
- Count a stop as one of the 30 ([testing.md](testing.md)).
- Treat the stop count as a third hurdle (plan).
- Place an order.

## No-view

**Does.** On a shut gate, the run publishes the evidence table, the words `no view`, and empty lists (plan). The sector label is `no view`, both name lists are empty, and the bull and bear sentences are absent (plan). A `no view` note does not open a sign (plan).

**Strategy.** The desk prints what it measured and refuses a view. That is the published product for as long as the gate is shut. It is the product this repo can describe today, because the episode count is unknown.

`Inference:` the chart sends a shut gate to this node and draws no edge from here to bull, bear, the narrator, or the walk-forward line. Those nodes do not run on this path (plan, for bull and bear). The empty-note skeleton still has a field for a walk-forward line or the words `no track record` ([execution.md](execution.md)). This page does not add a replay edge the chart does not draw.

**Owner.** Code writes `no view` and the empty lists (plan). No language-model sentence runs (plan).

**Inputs and outputs.** Input is a shut publish gate. Output is the evidence table, the words `no view`, and empty lists (plan).

**Must not.**

- Run bull or bear (plan).
- Fill either name list (plan).
- Publish a sector return, a rank, or a name (plan).
- Open a sign (plan).
- Let a repair add a view without facing the gate again (plan).
- Place an order.

A `no view` counts as an episode for this cell once the sector model wrote a signed expected excess here and that label is resolved and non-overlapping ([testing.md](testing.md)). The published words `no view` are not the label, and they do not drop the excess. A cell the model left unscored does not count. The sign rule is unchanged: a `no view` note does not open a sign (plan).

## Bull

**Does.** Bull runs only after the gate is open (plan). It speaks once (plan). It cites a row (plan). It states what would confirm the sector label (plan). It does not see the bear draft (plan). It has no tool that changes a rank (plan). There is no second round (plan).

**Strategy.** The confirming sentence comes after the number, and it can only point at a row that already exists. One turn, blind to the other side, so the two sentences cannot talk a number into existence.

**Owner.** The language model writes the sentence (plan). Code already owns the label it confirms and the figure it cites. The sentence does not own a number.

**Inputs and outputs.** Inputs are the open gate, the evidence table, and the sector label. Output is one sentence that cites a row and states what would confirm the label (plan).

**Must not.**

- Run when the gate is shut (plan).
- Speak twice, or see the bear draft (plan).
- Emit a return, a rank, or a topic score (plan).
- Change a rank, or add a name (plan).
- Place an order.

## Bear

**Does.** Bear runs only after the gate is open (plan). It speaks once (plan). It cites a row (plan). It states what would invalidate the sector label (plan). It does not see the bull draft (plan). It has no tool that changes a rank (plan). There is no second round (plan).

**Strategy.** The invalidation is one sentence bound to a row. It is the risk the dashboard will show. It is not a short, not a stop, and not a second model.

**Owner.** The language model writes the sentence (plan). Code owns the label and the cited figure. The sentence does not own a number.

**Inputs and outputs.** Inputs are the open gate, the evidence table, and the sector label. Output is one sentence that cites a row and states what would invalidate the label (plan). The bear does not receive the bull draft (plan).

**Must not.**

- Run when the gate is shut (plan).
- Speak twice, or see the bull draft (plan).
- Emit a return, a rank, or a topic score (plan).
- Name a short, change a rank, or add a name (plan).
- Place an order.

## Narrator

**Does.** The narrator turns the table and the two sentences into the dashboard (plan). The dashboard shows the topic, the sector label, the best and worst names, the opportunity, the risk, and the checklist (plan). The label was computed upstream (plan). The narrator does not write numbers (plan). The narrator cannot add a name (plan). It sees the table and the two sentences (plan).

**Strategy.** The dashboard is a rendering of decisions that code and the small stats model already made. The opportunity sentence and the invalidation sentence are the bull and the bear. The narrator does not get a new vote.

**Owner.** The language model writes the sentences that stitch the page together (plan). Code owns every figure, the label, the lists, and the checklist verdicts that are recomputed later. The narrator owns no number.

**Inputs and outputs.** Inputs are the evidence table, the bull sentence, and the bear sentence (plan). Output is the dashboard fields in the empty-note skeleton: topic id, evidence rows, sector label, best names, worst names, opportunity sentence, invalidation sentence, walk-forward line or `no track record`, risk verdict, checker verdict ([execution.md](execution.md)). The skeleton is a target shape, not a live pull (plan). The risk verdict and the checker verdict are filled by the nodes after this one.

**Must not.**

- Write a number (plan).
- Add a name (plan).
- Change the topic, the label, or the rank (plan).
- Reopen bull or bear (plan).
- Emit a return, a rank, or a topic score (plan).
- Place an order.

## Walk-forward base rate

**Does.** The replay is the walk-forward hit rate of this same scorecard, shown beside the call (plan). If it has not been computed, the note says there is no track record (plan). It is not a Monte Carlo of intraday bars (plan).

**Strategy.** The call sits next to the record of the same scorecard, built under the testing contract, or it sits next to an honest blank. Today the blank is the only legal output. No test has been run. This node does not invent the hit rate the gate's 9-point sketch talks about. That sketch is an assumption, and it is not this node's output (plan).

The contract, if a test is ever run, is the sequence in [testing.md](testing.md): freeze the rules first, point-in-time membership, Hang Seng TECH from launch, filing timestamps, flow vintage, trailing beta that ends before the decision, the Stock Connect split, purged overlapping labels, a refit per market and topic type, a fill at the next bar, and sector excess kept separate from traded P&L. The two baselines are shrunk-to-zero and the sign of own-sector momentum (plan). The testing page does not crown a winner. There is no output yet.

**Owner.** Code (plan). A language model does not own the hit rate. There is no hit rate in this repo to own.

**Inputs and outputs.** Inputs are the frozen scorecard and resolved, non-overlapping episodes from the same market and topic type. Output is the walk-forward line, or the words `no track record` (plan). This repo's output is `no track record`.

**Must not.**

- Invent a hit rate, a Sharpe, or a backtest. None exists here.
- Run a Monte Carlo of intraday bars (plan).
- Count overlapping weeks as episodes (assumption).
- Count an episode that has not reached the end of its horizon (plan).
- Drop a resolved label because the note was `no view`, blocked, or failed ([testing.md](testing.md)).
- Count an insufficient-data stop as an episode ([testing.md](testing.md)).
- Count a repair as a second episode ([execution.md](execution.md)).
- Include the decision bar in the label ([testing.md](testing.md)).
- Pool markets or topic types ([testing.md](testing.md)).
- Add sector excess and traded P&L into one number ([testing.md](testing.md)). The default graph has no orders, so traded P&L is empty (plan).
- Use the reported episodes to choose the gate, the rank key, or the floors ([testing.md](testing.md)).
- Place an order.

## Risk gate

**Does.** The risk gate is code (plan). The verdict is `PASS` or `BLOCK`. It checks the liquidity floor, same-market peers, a filled transmission slot for any Hong Kong to US link, and fresh data (plan). It is not a panel of risk personalities (plan). `BLOCK` publishes a blocked note and stops (plan).

**Strategy.** The gate restates, as a hard check, constraints the rank and the slot already claim. It is one verdict. It is not a second research pass, and it is not three agents arguing about risk. A `PASS` means those four checks cleared. It does not mean the excess is different from zero. That question belongs to the publish gate, whose width is unknown. It does not mean the name can be traded. Crowding, borrow, Hong Kong short-sale rules, and gap risk are out of scope (plan).

**Owner.** Code (plan). A language model is banned from the risk gate (plan).

**Inputs and outputs.** Inputs are the liquidity floor at the frozen 7.80 comparison, the peer set, the transmission slot if a Hong Kong to US link is claimed, and the vintages. Output is `PASS` or `BLOCK`. The USD level of the floor is still unknown until it is frozen (plan). `Inference:` the spec does not say the gate passes while that level is unknown. It says the level is unknown until the freeze (plan). This page does not invent a pass.

**Must not.**

- Split into risk personalities (plan).
- Change the score, the rank, or the topic (plan).
- Treat crowding, borrow, Hong Kong short-sale rules, or gap risk as checks. They are out of scope (plan).
- Treat `PASS` as permission to send an order. No node places an order (plan).
- Place an order.

## Blocked note

**Does.** On `BLOCK`, the run publishes a blocked note and stops (plan). A risk-gate block ends the run (plan).

**Strategy.** The block is the product. The run does not continue to the checker, the repair, or a softer wording of the same names.

**Owner.** Code owns the `BLOCK` verdict (plan). There is no language-model rewrite on this path.

**Inputs and outputs.** Input is `BLOCK`. Output is a blocked note, and the run ends (plan). The spec does not say this note opens a sign. That gap stays open. The note counts as a walk-forward episode when this cell's label is resolved and non-overlapping ([testing.md](testing.md)). The block does not erase the label.

**Must not.**

- Continue to the checker or the repair. The chart ends on this node.
- Replace the block with a smaller list or a different topic.
- Place an order.

## Checker

**Does.** The checker does not see the drafts or the topic rationale (plan). Code recomputes every cited number with the same tools (plan). A separate language model checks only whether each claim is entailed by the evidence table (plan). It does not get a second chance to improve the thesis (plan).

The chart's outcomes are pass, first failure, and second failure. Pass goes to the published note. First failure goes to one repair. Second failure goes to the failed note.

The checklist is closed (plan):

- The primary source is present.
- The baseline is recomputed.
- The liquidity floor is met.
- The reason contains a figure from the table.
- The sector score is not copied across markets.
- The topic is unchanged on revision.

**Strategy.** The checker is a new context so it does not share the writer's blind spot (plan). Recompute catches a number that drifted. Entailment catches a sentence the table does not support. Neither job is allowed to improve the thesis, because a rewrite is how a thin note becomes a fluent one. The checklist is closed so a new item cannot appear after a path is seen.

**Owner.** Code owns the recomputed numbers (plan). A separate language model owns only the entailment check (plan). Neither emits a score (plan).

**Inputs and outputs.** Inputs are the evidence table, the claims, and the recompute tools (plan). The checker does not receive drafts or the topic rationale (plan). Output is pass, or a first failure routed to repair, or a second failure routed to the failed note.

`Inference:` a figure that fails recompute is the "bad figure," and a claim that fails entailment is the "bad sentence." The spec names those two return paths (plan) and does not name which component labels them.

**Must not.**

- See the drafts or the topic rationale (plan).
- Improve the thesis (plan).
- Emit a return, a rank, or a topic score (plan).
- Add a checklist item that was not frozen ([testing.md](testing.md)).
- Allow a second repair (plan).
- Change the topic (plan).
- Place an order.

## Published note

**Does.** A checker pass publishes the note (plan). One run's note has a topic, evidence, a sector opportunity and risk, a short best list, a short worst list, and a quality-check verdict (plan). While the gate is shut, this node does not run. The shut path is `no view`.

**Strategy.** This is the only path that publishes a sector label and names. It is still a research note. Expected excess is a research label (plan). The publish gate having opened, and the checker having passed, is not a measured edge. [returns.md](returns.md) says surviving the advocate means the plan does not pretend to have earned 15% a year, and that this is not a measured edge. The process has not been backtested. The note is not safe to trade.

The paper sleeve in [returns.md](returns.md) is not this node and is not on this graph (plan). It may exist only after the gate passes, as a separate page: one sector ETF against the local index ETF, flat at invalidation or at expiry, a loss limit outside ordinary weekly noise, shut off after 500 basis points of drawdown from peak (plan). The numeric weekly limit is unknown until it is frozen before any sleeve test (plan). The sleeve does not feed the next note and does not trade the best and worst lists (plan). This spec states no Sharpe for that sleeve. The sleeve does not convert the assumed class range into 15% a year (plan).

**Owner.** No new number. Code owns the figures the note displays. The language model owns only the sentences already produced by bull, bear, and the narrator.

**Inputs and outputs.** Input is a checker pass after `PASS` on the risk gate. Output is the note. The fields start empty in the skeleton and are filled only by the nodes above ([execution.md](execution.md)).

**Must not.**

- Place an order, size a portfolio, or name a short (plan).
- Claim 15% a year, a hit rate, or a Sharpe. A 15% a year claim is not supported (plan). This spec claims neither Sharpe mark in [returns.md](returns.md).
- Trade the best and worst lists. The sleeve, which is off this graph, is barred from that too (plan).
- Feed this note's P&L into the next topic. The sleeve does not feed the next note (plan). The default graph has no P&L to feed, because it places no orders (plan).

## Failed note

**Does.** A second checker failure publishes a failed note (plan). A second failure ends the run (plan).

**Strategy.** The failure is published, so the run cannot quietly try a third wording. The topic was not re-picked. The run stops.

**Owner.** Code records the failed verdict. A language model does not get another pass to improve the thesis (plan).

**Inputs and outputs.** Input is the second checker failure. Output is a failed note, and the run ends (plan). The spec does not say this note opens a sign. That gap stays open. The note counts as a walk-forward episode when this cell's label is resolved and non-overlapping ([testing.md](testing.md)). The failure does not erase the label.

**Must not.**

- Repair again (plan).
- Re-pick the topic (plan).
- Hide the failure behind a `no view` or a blocked note. Those are different endings.
- Place an order.

## One repair

**Does.** One repair is allowed (plan). A bad figure returns to the sector model (plan). A bad sentence returns to the narrator (plan). The topic stays unchanged (plan). The return to the sector model restates the figure the checker recomputed (plan). The repair does not refit (plan). It does not change coefficients, the training window, the features, or the topic (plan). The repair edge does not return to topic choice (plan). It does not skip the publish gate (plan). A bad figure must face the gate again (plan). A repair is not a second episode (plan). A second checker failure publishes a failed note (plan).

The chart sends a bad figure back to the sector model, which then goes through the stock rank and the publish gate. The chart sends a bad sentence back to the narrator, which is downstream of the gate. Bull and bear have already run only because the gate was open (plan). A sentence repair is not a route onto that path from a shut gate.

Tool retries, capped at 3 inside a fetch, are not this repair (plan).

**Strategy.** The loop may correct the failed state and may not shop for a new topic after the prices are in. One trip. The topic lock is the control against data-mining a better story. The figure path faces the publish gate again so a repaired number cannot skip the hurdle that blocks bull and bear. `Inference:` this is one repair in total, not one per failure type. The spec says one repair is allowed, and a second failure publishes a failed note (plan).

**Owner.** Code routes the return. A bad figure lands on the small stats model. A bad sentence lands on the language-model narrator. The route does not emit a score of its own. Which component decides "figure" versus "sentence" is the inference under the checker. The sector-model return restates the recomputed figure and does not refit (plan). [execution.md](execution.md) owns that ban. [testing.md](testing.md) keeps the walk-forward refit on the other side of it.

**Inputs and outputs.** Input is the first checker failure. Output is a return to the sector model or a return to the narrator, then the path those nodes already have, including the checker again. The next failure ends at the failed note (plan).

**Must not.**

- Return to topic choice (plan).
- Start another bull and bear round (plan).
- Skip the publish gate (plan). A bad figure must face it again (plan).
- Repair twice (plan).
- Add a name or write a new number on the way through (plan).
- Treat a fetch retry as this repair (plan).
- Refit the ridge or the scorecard, or change coefficients, the training window, or the features (plan).
- Count the repair as a second episode (plan).
- Place an order.

## Devil's advocate

Two voices review the design below. They are written for this page. They are not quotations, and J.P. Morgan did not issue them. They are comments on the design and the strategy. They are not rules. They do not add a node, a threshold, a vendor, or a backtest. They do not soften [returns.md](returns.md).

Whether the annual return will be larger than 15% is answered in [returns.md](returns.md). Both comments there say no. These comments do not soften that answer.

The returns page already says the following, and both voices leave it standing. The user wants 15% a year (plan). That figure is a target, not an estimate from this sample, and the claim is not supported. The prior review put this class at about -5% to +4% a year of sector excess versus the local index, with the mass near zero (assumption). That range is not a backtest of this repo. A result near the middle is about zero (assumption). A result at the top is about 4% a year of sector excess (assumption). The gap from that top to the 15% target divides to 3.75 on those approximate inputs (arithmetic in [returns.md](returns.md)). The multiple is not a tested lever. Concentration, leverage, and a different strategy each fail this sample. The process has not been backtested. The note is not safe to trade.

### A J.P. Morgan quantitative researcher

No. I will not say this desk's annual return will be larger than 15%. The answer is in [returns.md](returns.md). The graph is a drawback control. I would not describe it as a forecast. The center of the excess is zero until a walk-forward exists. Nothing below is a measured bias. No test has been run.

**Session calendar.** Five, ten, and twenty sessions are written clocks, not estimated half-lives. They sit beside a 1 to 4 week label, and the spec does not derive one from the other. A sign can expire while its label window is still open. The purge of overlapping labels is the research control, and it lives in the testing page, not in this node.

**Parallel ingest.** The node is not executable as research until the point-in-time tapes exist. Free bars, a live consensus page, and a current constituent list fail the testing contract. A leak at this node is not repaired later. The testing page says a later step does not repair an earlier leak. A blended Stock Connect file can still enter the building. The ban on northbound is a ban on use. The spec does not draw a separate edge that drops those rows at ingest. I would not put northbound back into the feature set. I would not pretend a blended file was never read.

**Required-rows gate.** The predicate stays unlisted. The prose names holes that depend on a topic this gate has not scored. A gate I cannot replicate is not yet a control. I am not filling in the list.

**Insufficient-data stop.** Stopping is the right control. A stop is not an episode. The sector model wrote no label, so there is nothing to resolve, and the stop does not increment the 30. The scored cell can still be the weeks when the files were complete enough to label. That selection is stated. It is not a measured bias. I am not turning a stop into a label.

**Topic score.** A max across four robust z-scores will favor the feed that shouted. This repo has not measured that selection. The tie-break is a written order, not a weight. Breadth depends on a "touch" the spec does not define. Calling news the weakest topic loses a tie. It does not stop a high z-score on a headline from winning outright. Embeddings can reject secondary copy. They are not a test that the primary document identified anything.

**Lagged flow residual.** Residualizing lagged flow on the same-window return is the right control for a print that restates the price. It is not an identified premium. The beta window must end before the decision, and the length stays unpublished. I am not filling one in. A length chosen after a path is seen is a new test. The testing page keeps a restatement after the decision out. The data page says a complete free revision archive of southbound is unknown. The same residual then enters the topic score and the sector model. A topic that flow won is explained with flow. That circle breaks only if a walk-forward separates them. None has been run. Raw net buy stays out. I am not putting it back.

**Primary extract.** The next gate checks presence. Presence is not identification. The extract can take the convenient figure from a long primary document, and the stats tool will compute surprise on the fields it was given. The checker recomputes the rows it receives. A faithful recompute of a biased extract still passes.

**Filing extract.** Separate schemas are the right control. The shortlist is undefined at the moment this node runs, because the rank has not run. If the shortlist is not the topic's sector names, the node has no input. Nothing in the node, other than the schema split, stops a figure from one market being read against the other market's baseline once both sit in one table.

**Price and volume.** Sixty sessions and a 20-session median are written windows. They were not chosen by a test in this repo. The outputs are descriptions of sector ETFs and the index. They are not a model of 1 to 4 week excess. The 20-session relative return the rank shows is not pinned to a node. A column sitting beside a rank will be read as the signal. The spec says it is not a rank key. The layout still invites the misread.

**Evidence table.** One citable table is the right boundary. Raw net buy stops at the vintage and does not enter as a score. The checklist says the reason contains a figure from the table. It does not name the column. A sentence can cite a raw figure that the vintage still holds. The control depends on the writer citing the residual.

**Primary-row gate.** "Valid" is not defined past "missing." A present row from the right host can still be the wrong figure. The gate will pass it.

**Sector model.** This is the only small stats model, and the design puts the published excess on zero until a walk-forward says otherwise. No walk-forward exists. The features include own-sector momentum and the lagged flow residual. The testing page says a residual that only restates the momentum sign has not added a signal. That comparison has not been run. The 5% slot floor is frozen in name only, because the denominator is unknown. An unfrozen feature cannot be walked forward, and freezing it after a seen path is a new test. Rate beta stays out of the slot. I am not asking for it back. The repair can return a bad figure here. It restates the recomputed figure and does not refit. A refit would have been a second look at the same label. The ban closes that look. It does not create a measured excess.

**Stock rank.** The key has no weights, and the spec forbids a composite score. Two implementations can both claim they followed the page and order the names differently. The USD liquidity floor is unfrozen, so the filter is not replicable yet. The cap of 3, once a record exists, is a concentrated book. The returns page already says there is no tested path from that cap to 15% a year. Dropping every name with an event inside the horizon removes the weeks when the fundamental anchor is most informative. That bias is not measured.

**Publish gate.** Thirty episodes and half the trailing residual error are assumptions. The about-9-point hit-rate sketch is not the residual error. The spec says so, and a reader will still mix them. An unknown count fails, so the gate is shut, and the research output today is `no view`. Thirty episodes are, on the spec's own words, enough for a sign only. An open gate later would be a hurdle clearing. It would not be a finding that the excess is non-zero.

**No-view.** This is the honest node. A `no view` counts toward the 30 when the sector model wrote an excess and that label is resolved and non-overlapping. The published words are not the label. The weeks inside the noise stay in the cell. Counting them does not open the gate. A cell the model left unscored is not an episode. I am not adding a hit rate for either case.

**Bull and bear.** One cited sentence each, blind to the other, blocks a debate that invents a rank. It adds no information the table did not already hold. Both sentences can be entailed and still be the two halves of noise. They never see the weeks the gate called noise, because they do not run when the gate is shut. The prose is reviewed on the tail.

**Narrator.** The narrator does not write numbers. The dashboard still puts the label, the names, and the 20-session relative return in one view. The skeleton has no field that says the relative return is not a rank key. A faithful rendering can read as a momentum book.

**Walk-forward base rate.** The node is empty. The only honest sentence is that there is no track record. There is no hit rate and no Sharpe beside the call. Shrunk-to-zero and the sign of own-sector momentum have not been compared. Until that comparison exists, the center of the excess is the shrunk-to-zero line. The class range on the returns page is an assumption from a prior review. It is not a confidence interval for this graph.

**Risk gate.** The four checks do not ask whether the excess is distinguishable from zero. A `PASS` is a statement about the floor, the peers, the slot, and the vintage. Crowding, borrow, short-sale rules, and gap risk are out of scope, so the gate cannot fail them. A label can pass and be untradeable. That is the spec. It is why a `PASS` is not a result.

**Blocked note, published note, failed note.** A checker pass will be read as the call. The returns page says survival is not a measured edge, and that a 15% a year claim is not supported. The pass does not change that arithmetic. A blocked note and a failed note enter the walk-forward when they carry a resolved, non-overlapping label. The stop does not. The ending is not a filter on the cell. The count is the testing page's, and it is not a result. The spec still does not say a blocked note or a failed note opens a sign.

**One repair.** The topic lock is the control that matters. The return to the sector model restates the recomputed figure and does not refit, so the lock is not a second estimation. A sentence repair goes to the narrator, downstream of the gate, which matches the sentence that a bad figure must face the gate again. Entailment of the repaired sentence is not a second model.

No. I will not say the annual return will be larger than 15%. Nothing in this review closes the gap from a mass near zero to that target. Concentration at three names, leverage, and a different strategy fail this sample for the reasons the returns page gives. Leverage on a mass near zero scales noise, including the loss end of the assumed range. I have no Sharpe to put on the sleeve, and the spec states none.

### A J.P. Morgan trader

No. I will not say this desk's annual return will be larger than 15%. The answer is in [returns.md](returns.md). I cannot use this note. The note is not safe to trade. That is not a request for an order node. The spec has no order node, and I am not adding one.

**Session calendar.** Hong Kong and the US do not share a close. The decision close is the session close of the market the label belongs to, the close of that market's daily bar. I cannot use the other market's close, and a holiday does not borrow one. That tells me which bar is forbidden. It is not a clock I can run a book on. Expiry at 5, 10, or 20 sessions is not a risk meeting. The spec has no position, so it has nothing to say about a position that outlives the sign.

**Parallel ingest.** Southbound in this design is day-end. If it is stale, the desk substitutes HKEX turnover concentration. Concentration is not a buy and not a sell. I cannot lean on it before the close, and I cannot match it to the tape on my screen after the close. US ETF flow with a vintage is a paid tape this repo has not attached. Northbound is not a Hong Kong feature. The series a Hong Kong desk argues about is absent. This note fails as a flow product. I am not asking to put that series back.

**Required-rows gate.** A short file ends in a stop. I cannot fill the hole with a broker quote and continue. On a morning when the feed is late, the desk is silent.

**Insufficient-data stop.** The stop is not an episode. Silence is not a flat I chose. The stop does not say hold, cut, or stay out. It does not close a position, because the graph never opened one.

**Topic score.** One topic is one story. A book is several. The tie-break is macro, then filings, then flow, then news. News alone is the weakest topic. The note will often be a calendar print, or it will be `no view`. Neither replaces the meeting.

**Lagged flow residual.** The number on the page is a residual after the same-window return, lagged, with a beta window whose length stays unpublished. I cannot hedge that residual. The raw buy and sell, which is the print I would compare with the exchange page, is not allowed to be the score. That is the right research ban, and it makes the row useless as a blotter. The residual will not match the page on the screen.

**Primary extract.** I get a schema row from an official document. I do not get a level or a session I can hit. Release time and acceptance time are the timestamps, and this run is not a low-latency reader of them. The next-bar rule has already moved the fill off the bar the document hit.

**Filing extract.** I do not get a comparable EPS across Hong Kong and the US. The spec forbids that comparison by splitting the schemas and by keeping peers inside one market. The node fails that use on purpose. A name with the filing inside the horizon is then dropped at the rank. The note can call a filing the topic and then refuse to name the stock.

**Price and volume.** I am handed a 60-session return, a realized vol, and a volume versus its 20-session median, for sector ETFs and the index. I am not handed a level, a stop, or a size. The 20-session relative return will sit on the name table. If I sort by it, I have left the spec. The page will still let my eye do it.

**Evidence table.** When the gate is shut, the table is the whole product. I can read a surprise. I cannot turn it into an order. Each print keeps its currency. The only conversion is 7.80, and that constant is not the rate I deal at. There is no FX hedge in the MVP.

**Primary-row gate.** A recap the street is trading on is a reject. I can be looking at the same tape as everyone else and still receive nothing from this desk.

**Sector model.** The label is a signed expected excess, shrunk hard toward zero, and unpublished until the gate opens. I cannot put it on as a position. There is no size. An empty slot drops the Hong Kong names off a US story. Rate beta, which is how the two books move together on a rates day, cannot fill the slot. On the day I want one view, the note keeps two markets apart. That is the spec. It fails as a cross-market tool. I am not asking to legalize rate beta.

**Stock rank.** The cap is 0 until a record exists. I opened the note for names. There are none. After a record, the cap is 3 names a market, with no short and no size. A name with earnings inside the horizon is dropped, and that is the name the meeting is about. The worst list never names a short. I leave with no hedge.

**Publish gate.** The gate is shut. The episode count in this repo is unknown, and unknown fails. Half a residual error cannot be computed, because the error is unknown until the episodes exist. Bull and bear do not run. A US flow record does not open a Hong Kong macro note. The cell I trade is not a cell that has history.

**No-view.** This is the note I will actually receive. Evidence, the words `no view`, empty lists. It does not open a sign. If the sector model wrote an excess, the week still counts as an episode once the horizon ends. The words are not the label, and the count is not a flat. I cannot book `no view` as a flat. The desk did not say flat. It said nothing.

**Bull.** One sentence, one row, what would confirm the label. No price, no size, no time. I cannot trade a confirmation written that way.

**Bear.** One sentence on what would invalidate the label. Not a stop and not a level. There is no second round where I can ask for the level. The spec ends the conversation there.

**Narrator.** The dashboard cannot add the name I wish were on the list, and it cannot write the number I wish I had. That is the control. It is also why I cannot use the page to finish a list.

**Walk-forward base rate.** The line says there is no track record. I cannot show a hit rate I do not have, and I cannot show a Sharpe. A risk committee that asks for 15% a year will not find it beside the call. The target is a target. Inventing a hit rate for the committee would falsify the node.

**Risk gate.** `PASS` checks a liquidity floor whose USD level is unfrozen, same-market peers, a filled slot, and fresh data. It does not check borrow, a locate, Hong Kong short-sale eligibility, or the gap into the next session. Those are out of scope. I have seen a `PASS` that meant I could send an order. This `PASS` does not mean that.

**Blocked note.** The run stops. There is no alternate name, no smaller size, and no instruction to use the sector ETF. The sleeve that holds a sector ETF against the local index ETF is not on this graph. I cannot override the block. There is no human-yes node.

**Checker.** A pass means the numbers recompute and the sentences follow from the table. I would read "pass" as a green light. On this desk that reading is wrong. The checker is not allowed to take a trader's question and improve the thesis. One repair is for a bad figure or a bad sentence, not for "I cannot use this."

**Published note.** This is the document a reader will forward to an execution desk. Forwarding it is a misuse of every node above. The note places no order and sizes no book. Hong Kong stamp duty is 0.1% a side from 17 November 2023 (checked, in the data page). A round trip is 0.2% (arithmetic on the returns page). The yearly bill is unknown until turnover is frozen. The US commission is unknown. I will not invent one. Against an excess whose assumed mass is near zero, I still do not have a net number. The returns page says the plan does not pretend to have earned 15% a year, and that survival is not a measured edge. The sleeve stays off the graph, states no Sharpe, and does not convert the assumed range into the target. I still cannot run that sleeve from this page. The weekly loss limit is unknown until it is frozen.

**Failed note.** The second failure publishes the failure and stops. I do not get the evidence dressed as a call. I also do not get a sentence that tells me whether a previous sign is void. The spec does not say. I would need that sentence to run a book, and it is not here.

**One repair.** If the topic is the wrong story, the repair will not change it. The repair does not refit, so it will not estimate a better story after the check fails. A bad figure faces the gate again, so a name can disappear into `no view` on the second pass. A bad sentence returns to a narrator who still cannot add a name or a number. There is no path from this node to an order.

No. I will not say the annual return will be larger than 15%. The highest-return plan that survives the returns page is still this graph, with the publish gate. Surviving means the plan does not pretend to have earned 15% a year. It does not mean a measured edge. A 15% a year claim is not supported. The process has not been backtested. The note is not safe to trade.
