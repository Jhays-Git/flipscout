# FlipScout

AI-assisted resale price research and deal tracking for small online sellers. Built for an MGMT 3000 AI project.

**Live site:** https://jhays-git.github.io/flipscout/

## What it does

- **Price check.** Describe an item (Pokémon cards and sealed product, laptops and tech, furniture). The site writes a strict research prompt for any AI tool with web search. Paste the JSON answer back and FlipScout validates the comps, leaves out outliers and wrong variants, and works out a quick sale, list and patient price, the profit after fees and shipping, and the most you should pay.
- **Deal feed.** Keep a watchlist, generate a scan prompt, import the agent's results, and filter, save, dismiss or mark deals as bought. Profit is recalculated on the page, and estimates that are higher than the agent's own sold evidence are lowered to match it.
- **History.** Price checks and unsaved deals expire after 30 days (editable) unless pinned or saved.
- **Profit rating on a sliding scale.** Margin thresholds depend on what the item costs, with a minimum dollar profit for each range.

## How it is built

One static `index.html` with no build step and no backend. All data stays in the browser (localStorage). Pasted AI output is treated as untrusted: it is shown as plain text and only http or https links are made clickable.

## Limits

Sold prices are often hidden by marketplaces, so many results rely on asking prices and are marked lower confidence. Fee rates and shipping costs are editable assumptions. Results are estimates, not financial advice. Nothing here buys or sells anything.
