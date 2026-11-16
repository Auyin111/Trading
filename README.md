# Hong Kong and US research desk

This repo holds the spec for one equity research run on Hong Kong and the US. The pages are a plan. They are not a backtest. No return in this repo is a result.

## What one run does

One run builds one note, or it stops. The note carries a topic, an evidence table, a sector label, and stock lists. Code owns the topic, every figure, and every rank. A language model extracts primary documents into a schema and writes sentences that cite table figures. It does not emit a return, a rank, or a topic score.

Missing required rows end the run as insufficient data. A shut publish gate still prints the evidence, the words `no view`, and empty lists. Bull and bear do not run on that path. The chart, the gate, and the repair rule are in [docs/execution.md](docs/execution.md).

## MVP

Markets are Hong Kong and the US (plan). The horizon is 1 to 4 weeks (plan). The universe is Hang Seng, Hang Seng TECH, and S&P 500 (plan). The plan sketches that set at about 600 names (plan). That sketch is not a live count.

The MVP places no orders (plan). It does not size a portfolio (plan). It does not name a short (plan). The name cap is 0 until the publish gate has a record, then 3 names per market (plan).

The publish gate is code (plan). It stays shut if that market and topic type have fewer than 30 resolved walk-forward episodes (assumption), or if the shrunk score sits inside half the trailing residual error (assumption). Thirty and the error width are planning assumptions. They are not a fitted result. The width is unknown until those episodes exist.

## Where the detail is

- [docs/execution.md](docs/execution.md) is the run, step by step, including where a language model is used and where it is banned.
- [docs/nodes.md](docs/nodes.md) is each node in that run: the job, the strategy, who owns the number, and what it must not do.
- [docs/data.md](docs/data.md) is the data the run requires and where to get it.
- [docs/testing.md](docs/testing.md) is how to test without look-ahead.
- [docs/returns.md](docs/returns.md) is the case against a 15% a year target (plan).

A 15% a year claim (plan) is not supported.
