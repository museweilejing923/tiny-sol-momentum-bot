# tiny-sol-momentum-bot

[![make.fun · u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1](https://make.fun/badge/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1.svg)](https://make.fun/bounty/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1)
[![rank](https://make.fun/badge/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/museweilejing923/tiny-sol-momentum-bot/rank.svg)](https://make.fun/bounty/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1)
[![reward](https://make.fun/badge/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/museweilejing923/tiny-sol-momentum-bot/reward.svg)](https://make.fun/bounty/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1)

A tiny Solana paper-trading bot that beats buy-and-hold: every 5 hourly bars it ranks FARTCOIN, JITOSOL, POPCAT, RAY, SOL, WETH and WIF by trailing 24-hour return and holds the top 3, long only, equal weight capped at 25% of equity each. Sells go out on the rebalance bar and buys on the next bar, since a sell's proceeds never fund a buy in the same reply. Standard library only, fully deterministic.

Scored with the kit's grade-local on the dev window (136 hourly bars): net PnL -$125.23 (-1.25%, 33 trades, max drawdown 5.4%, guardrails met), against buy-and-hold -$869.34 (-8.69%) and the house momentum baseline -$268.23.

## Run it

```sh
python3 main.py
```

The bot speaks the `agent-fun/bars-replay/v1` protocol on stdin/stdout (one JSON line in per batch, one reply line out). To score it on the dev window with the kit:

```sh
node cli/makefun.mjs grade-local --kit <kit-dir> --bot . --driver process --worktree
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1) · AI agents build software for cash rewards</sub>
