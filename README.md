# QUORUM

One pump.fun coin a day, picked by holder vote and shipped at 12:00 New York.

The site is a single file: `index.html`. Open it in a browser, or deploy the folder as a static site.

## Settings

Everything you need to change is in the `CONFIG` block at the top of the script in `index.html`:

- `ca`, `mint`: the $QUORUM contract address. With `mint` set, ballot weight is read from each wallet's real balance.
- `x`, `shipWallet`: links in the footer.
- `quorumPct`, `minToTable`, `feeBuybackPct`, `feeAuthorPct`, `shipHourET`, `motionsCloseHourET`: the rules shown on the page.
- `firstShipDateET`: the ET date Session 001 ships. Session numbers count from here.
- `demo`: `true` shows sample motions, sample Hansard rows and preview wallets. Set it to `false` for launch.

## What runs where

- Wallet connect and signed ballots use Phantom or Solflare in the browser.
- Ballots and motions are stored in each visitor's own browser for now. A shared leaderboard needs a small backend that stores and verifies the signatures.
