What you’re asking about is essentially: “How do I see where the biggest bets are in the options market (i.e. which strike(s) have the most open interest / largest positioning)?” — and “How do pros use that information in their daily trading?”
I’ll break this down in two parts:
1. How to find the strike(s) with the most bets (i.e. where market interest is clustered)
In options markets, the common proxies for “where the bets are” are open interest and sometimes max pain (or “pin risk”) estimates. Open interest (OI) tells you how many option contracts are currently outstanding (not yet closed) at each strike + expiration — so a strike with very high open interest can indicate a lot of “betting” is concentrated there.
Here’s how you can do that in Tastytrade / Tastyworks and in ThinkOrSwim (TOS) / ThinkScript.
In Tastytrade / Tastyworks
In the options chain on Tastyworks, you can view the open interest for each strike and expiration period. The strikes with the largest open interest are often the ones with “most bets.”
Some traders will sort or filter by open interest or by “volume + OI” to see strikes that are heavily populated.
As expiration approaches, comparing OI distributions across strikes can help you see where the “pinning” or clustering is happening.
Tastytrade also publishes educational content about “max pain” theory (i.e. the strike where options sellers have the least liability) which is often overlaid on open interest distributions.
However, Tastyworks/Tastytrade doesn’t (to my knowledge) give a built-in “heatmap of max bets” like some specialized options analytics tools do (though third-party or chart-overlay tools might).
In ThinkOrSwim (TOS)
ThinkOrSwim is more flexible. You can:
Use the Options Chain / “Product Depth” view. There is a “Product Depth” (or “Option Metrics”) tab which will show you curves (e.g. open interest vs. strike) and highlight which strikes have the greatest open interest. 
YouTube
Use thinkScript: TOS provides a function open_interest() which returns the open interest for a given strike. 
Think or Swim Learning Center
You can build a study or overlay that shows (for the currently selected expiration) the top 3 or 5 strikes by open interest (both calls and puts).
There are community scripts (e.g. “Top 5 Highest OI Calls & Puts” indicator) that draw those strikes on your price chart. 
YouTube
+1
Use scans / filters: You can scan for options where volume > open interest or where OI is particularly high. 
useThinkScript Community
+2
Reddit
+2
Use the “Trade Flash” / Unusual Options Activity gadget or widget in TOS, which shows large trades as they print (which often coincide with bets opening at or near major strikes). 
YouTube
A caveat: open interest is updated end-of-day (not intra-day in many systems), so your snapshot may lag the real-time shifts in positioning. Also, extremely large trades (block trades) sometimes happen outside of the displayed chain before they get registered.
Another concept frequently used is “max pain / max pain theory” — the idea that as expiration approaches, the underlying often gravitates toward the strike where option sellers (writers) have the least liability (i.e. where the sum of open interest losses is minimized). This is controversial, but many retail and semi-professional traders use it as a reference point. 
Investopedia
+2
Option Samurai
+2
In TOS, there are thinkScripts people have shared that plot the “max pain” line on the chart. 
useThinkScript Community
+2
Reddit
+2
Some websites (like OptionCharts) compute max pain for you given open interest distributions. 
OptionCharts
So in short: you look at open interest (and changes in it), optionally overlay a max pain estimate, and see which strikes are the “heaviest” in terms of positioning.
2. How professional / sophisticated traders might use this information (day-to-day strategy)
Knowing where the bets are concentrated gives you insight into potential support/resistance zones, pin straddles, and where price might gravitate (or be pushed) especially near expiration. Here’s how pros often use this:
A. Identifying Support/Resistance and “Pin” Zones
If a strike has very high open interest, especially in both calls and puts, that strike can act like a magnet (or “pin”) near expiration. Price may tend to gravitate toward or struggle to move away from that level.
Traders will monitor how price behaves relative to those heavy OI strikes. If price is below a heavy OI strike, that strike might act as resistance. If above, it might act as support (depending on the split of calls versus puts).
Close to expiration, this effect (if present) can become stronger (because option sellers may hedge, or delta hedging dynamics come into play).
B. Fade or Align Trades Around the Clustering
If you see a very large concentration of open interest at a given strike, some traders will fade extreme moves away from that strike — betting that price will revert back.
Others will ride momentum if price breaks away decisively from that heavy strike, using the “pop or drop” hypothesis (i.e. once the pin is broken, there may be momentum).
Traders sometimes use straddle / strangle / iron condor strategies around high-OI strikes: e.g. shorting or buying protection around that zone.
C. Hedging / Dynamic Adjustments
Option sellers (i.e. market makers or professional volatility sellers) will monitor how far price is from heavy strikes and dynamically hedge their delta exposure. That hedging flow can influence price momentum.
If price moves close to a heavy OI strike, option sellers may start hedging more aggressively — pushing price.
D. Risk Management & Expiration Effects
As expiration approaches (especially same-day or 0DTE), the sensitivity of open interest / max pain clusters increases. Traders will watch whether OI at certain strikes is being “blown out” (i.e. big position squaring) which could lead to volatility.
Professionals use these OI/clustering insights to gauge where liquidity might be thin or where a squeeze could happen.
E. Combining with Other Indicators / Flow
OI / cluster data is rarely used in isolation. Pros combine it with volume, implied volatility, delta skew, order flow, time of day, news events, technical levels, etc.
They also watch changes in open interest (i.e. daily Δ OI) to see where new money is entering or old money exiting.
Practical Example (Day Trading Scenario)
Let me sketch a hypothetical daily flow:
Early in the day, you pull up the open interest distribution for your target stock (or index) for the nearest expiration. You see a particularly high concentration at strike X (call and put).
You overlay the max pain line (which is close to strike X).
You place “watch zones” around X (e.g. ± $2 or ± $5) as potential reversal or support zones.
If price drifts near X and stalls (with weakening momentum), you might take a mean-reversion trade (e.g. fade the drift).
If price breaks through X decisively, you might join the breakout direction, expecting that once the “pin” is broken, momentum may accelerate.
As you trade, you monitor order flow / volume to confirm whether there's genuine buying or selling pressure.
Late in the day, you may adjust or close positions approaching expiration, especially if price is very close to a heavy OI strike (because of increased pin / gamma effects).
Over many trades, the repeated observation of how price reacts around heavy OI strikes gives you probabilistic edges or warning zones.
Limitations & Caveats
Open interest is typically updated end-of-day; intraday shifts may not be fully reflected.
The “max pain / strike clustering causes price to gravitate” idea is debated — it does not always work, especially in highly trending or news-driven markets. 
Investopedia
+1
Large players can move markets, so clustering may sometimes be the cause after the move, not the reason for it.
It’s one tool among many — relying solely on OI clustering is risky.
Liquidity, bid/ask spreads, slippage, and order execution costs can erode advantages especially for retail traders.
If you like, I can walk you through a step-by-step tutorial (with screenshots or scripts) on how to do this in ThinkOrSwim (e.g. build a thinkScript that shows top OI strikes, overlay max pain, and create alerts). Do you want me to guide you through that?
