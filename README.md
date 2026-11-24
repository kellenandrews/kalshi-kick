# kalshi-kick

Timer repo. Every 20 minutes it asks GitHub to run the `gas-bot` and `rain-bot` workflows in the private
`kalshi-paper` repo. It holds no data, no exchange keys and no trading logic — only a GitHub token
(`DISPATCH_TOKEN`: fine-grained, Actions read/write on `kalshi-paper` only) stored as a repo secret.

Why: GitHub's scheduler on the private repo fires only a couple of times a day, and the alternative was a
launchd job on a laptop. `fired.log` shows how often this timer actually ran.
