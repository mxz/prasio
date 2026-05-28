---
title: "The Wheel Strategy, Part 2: Selling Puts — The Entry Side"
date: 2026-05-28
draft: false
tags: ["options", "trading", "wheel strategy", "cash-secured puts", "investing"]
categories: ["Options Trading"]
description: "The put side of the wheel is where your income generation begins. Here's how to select a strike, size a position, collect premium, and manage the trade — including when things don't go to plan."
showToc: true
TocOpen: false
cover:
  image: ""
  alt: "Selling Puts — The Entry Side of the Wheel"
  caption: ""
series: ["The Wheel Strategy"]
---

> **Disclaimer:** This post is for educational purposes only and does not constitute financial advice. Options trading involves substantial risk of loss. Past performance is not indicative of future results. Consult a licensed financial professional before making any investment decisions. All examples are illustrative only.

---

_This is Part 2 of a 3-part series. If you haven't read [Part 1](/posts/wheel-strategy-part-1), start there — the mechanics below assume familiarity with options basics, strike prices, delta, and assignment._

---

## The Put Side, Put Simply

You identify a stock you're willing to own. You agree to buy it at a price below its current market value. You collect cash upfront for making that agreement. If the stock stays above your price, you keep the cash and do it again. If it drops to your price, you buy the shares — at a discount to where it was trading when you made the agreement.

That's the put leg of the wheel. Everything below is the implementation detail.

---

## Stock Selection: The Most Important Decision You'll Make

Before discussing strikes or expirations, this has to come first: **only sell puts on stocks you are genuinely willing to own at the strike price.**

This is not a cliché disclaimer. It's the load-bearing rule of the entire strategy.

When you sell a put, you are accepting a contractual obligation to buy 100 shares at the strike price if the stock drops there. The premium you collect does not protect you from a stock that falls 40% — it offsets a small fraction of the loss. If you wouldn't buy the stock outright, the premium is not sufficient compensation for taking assignment on it.

**Criteria for a wheel-eligible stock:**

- **You understand the business.** Not in depth — but you understand what drives the stock, what the major risks are, and why it might drop. Stocks you've never looked at are not candidates.
- **You're comfortable holding through volatility.** If the stock drops 20% after assignment, you'll be selling covered calls on a position that's underwater. That can take months to work through. If you'd panic-sell at the first drawdown, don't wheel it.
- **Sufficient liquidity.** Options on thinly traded stocks have wide bid-ask spreads — the difference between the price you can buy and sell an option. Wide spreads erode returns. You want tight spreads, high open interest, and active volume. Stocks in major indices with options volume in the thousands per day are appropriate. Avoid small caps and anything with sparse options chains.
- **Reasonable implied volatility.** Higher IV means richer premiums, but also means the market is pricing in real uncertainty. There's a sweet spot — stocks with enough volatility to offer meaningful premiums without being genuinely dangerous to own. Large-cap tech, financials, and well-established growth names often sit in this range.

The candidates that tend to work well: blue chip names, large-cap tech, major ETFs like SPY or QQQ, and established growth stocks with active options markets. The candidates that tend to blow up wheels: speculative biotech, pre-revenue companies, meme stocks, anything with binary event risk (drug approval, court rulings, earnings in the next 2 weeks).

---

## Setting Up the Trade

Once you have your stock, you need three decisions: **strike price**, **expiration date**, and **position size.**

### Strike Price Selection

Your strike price determines two things simultaneously: how much premium you collect, and at what price you'd be obligated to buy the stock. These are in direct tension. A higher strike (closer to current price) means more premium but higher assignment probability. A lower strike means less premium but more distance before you're at risk.

**Use delta as your selector, not a percentage.**

A common beginner mistake is selecting strikes by saying "I want to be 10% below the current price." That's not wrong, but it ignores implied volatility entirely. A 10% Out-of-The-Money (OTM) strike on a low-volatility stock might have a delta of 0.05 — you're collecting almost nothing. A 10% OTM strike on a high-IV stock might have a delta of 0.25 — meaningful premium and real assignment risk.

Delta tells you the probability-adjusted position you're taking, regardless of the stock's absolute volatility.

**Target delta for the wheel: 0.20–0.30.**

This puts you at roughly a 70–80% probability of expiring worthless and keeping the full premium. You're OTM but not so far out that the premium is negligible. It's an aggressive-enough position to generate income, conservative-enough to give the stock room to move against you.

For a more conservative posture, go 0.15. For more income at higher risk, 0.30–0.35. Don't go below 0.10 — the premium isn't worth the capital commitment.

**Translate delta to a price target:** If the stock is at $50 and you're targeting delta 0.25, look at the options chain and find the strike where the put delta is closest to 0.25. That might be the $46 or $47 strike depending on current IV. That's your strike — the price at which you'd be fine owning 100 shares.

### Expiration Date Selection

The wheel runs on **short-dated expirations** — typically 2 to 5 weeks out (14–35 days to expiration, or DTE).

The reason is theta decay. Time value doesn't decay linearly — it accelerates as expiration approaches. The last 2–3 weeks of an option's life is when decay is fastest. By selling options in the 2–5 week window, you're in the steepest part of the decay curve for the majority of the trade's life.

**Avoid weeklies (under 7 DTE) as a starting point.** The premium-to-risk ratio is poor — you collect a fraction of what you'd collect with 3 more weeks on the clock, but your delta can spike dramatically if the stock moves. There's not enough buffer. As you get more experienced with a position, short-dated management rolls make sense — but for entry, 21–35 DTE is the standard.

**Avoid going beyond 45 DTE.** Premium does increase with more time, but it scales sub-linearly — you're not collecting twice as much for twice the time. And you're tying up capital longer with less flexibility to respond to stock movements.

**The practical target: monthly expirations, 21–35 DTE at entry.** Most brokers display these clearly. For liquid stocks, these will have the tightest spreads and highest open interest.

### Position Sizing

This is where most new option traders undersize or oversize — both are mistakes.

**The cash requirement:** Selling a cash-secured put obligates you to buy 100 shares if assigned. If you sell a put with a $45 strike, you need $4,500 per contract in available cash or margin. That's the "cash-secured" part — you have the capital to fulfill your obligation.

**Never sell more puts than you can afford to be assigned on.** This is not a theoretical concern. Stocks drop. If you sell 10 contracts on a $50 stock ($50,000 in potential obligation) and don't have that capital available, you're using margin you may not be able to maintain. Forced liquidations at the worst possible time are how accounts blow up.

**Per-position sizing guideline:** No single put position should represent more than 5–10% of your total portfolio. If your account is $100,000, one put position should require no more than $5,000–$10,000 in potential assignment capital. This lets you run multiple positions simultaneously without any single stock's movement becoming catastrophic.

**Across all positions:** Keep total notional exposure — the total amount you'd spend if assigned on every open put — to 20–25% of your portfolio equity. This means most of your capital is still liquid and deployable, and you're not overcommitted to the downside in any market environment.

---

## Placing the Trade

In your broker's options interface, you're selling to open a put contract. The mechanics:

1. Select your stock and navigate to the options chain.
2. Choose your expiration (the column for your target date).
3. Find the put at your target delta (usually displayed in the chain — if not, a delta 0.25 put is roughly 1–1.5 standard deviations OTM).
4. Check the bid-ask spread. The mid-price is your target fill price — the midpoint between what buyers are bidding and sellers are asking. On liquid options, you can often get filled at or near mid.
5. Enter a limit order to **sell to open** at the mid-price. Don't use market orders on options — the spread will cost you.
6. You collect the premium immediately. It posts to your account the same day.

That's it. You've opened a position. You've collected income. Now you manage it.

---

## Managing an Open Put Position

The trade is live. Here's what to watch.

### The Default Outcome: Stock Stays Above Your Strike

If the stock stays above your strike at expiration, the put expires worthless. You keep 100% of the premium. No action required — the contract simply ceases to exist and your capital is freed up.

This is the expected outcome ~75% of the time when you're selling at delta 0.25. Repeat, and the income compounds.

### Taking Profits Early

You don't have to hold every trade to expiration. A common rule: **close the position when you've captured 50% of the premium, regardless of DTE remaining.**

If you sold a put for $1.50 and it's now worth $0.75 (because time has passed and/or the stock moved away from your strike), you can buy it back for $0.75 and close the trade. You've captured half the premium in potentially half the time — freeing up capital to redeploy in a new position.

The math favors this over holding to expiration. You reduce gamma risk (the risk of a fast move near expiration flipping your position from profitable to a loss), and you increase your annualized return by putting capital back to work sooner.

**50% profit is a guideline, not a rule.** At 21 DTE with 5 days elapsed, closing at 50% profit makes sense. At 3 DTE with most decay captured, holding to expiration is usually fine.

### When the Stock Drops Toward Your Strike

This is where discipline matters. The instinct is to panic and close early at a loss. The disciplined response is to evaluate your position methodically.

**If the stock is approaching but not yet at your strike:**

Check delta. If the put's delta has risen to 0.35–0.45, the market is now pricing more assignment risk into your position. You have options:

- **Hold:** If you believe the move is temporary and you're still comfortable owning at the strike, holding is valid. You collected premium for exactly this scenario.
- **Roll down and out:** Buy back your current put (at a loss) and simultaneously sell a new put with a lower strike at a later expiration, targeting a net credit or small debit. You reduce your obligation price, extend your time, and collect additional premium. This is the most common management technique.

The key question when rolling is: **is the new strike a price you're comfortable owning?** If you keep rolling further and further down to avoid assignment, you're hiding from the position, not managing it. Eventually you need to decide: am I willing to own this stock, or not?

**Rolling mechanics (briefly):** This is most cleanly executed as a single combination order — buy to close the existing put, sell to open the new put — so you execute both legs simultaneously at a net price. Your broker may call this a "roll" or a "spread order." Avoid legging into the two transactions separately; you take execution risk.

### Taking Assignment

If expiration arrives and the stock is below your strike — or if you choose to let the assignment happen — you'll wake up with shares in your account and no put position.

Your effective cost basis on the shares is: **strike price minus premium received per share.**

Example: You sold a put with a $45 strike and collected $1.20 in premium. The stock is at $43 at expiration. You're assigned 100 shares. Your cost basis is $45.00 − $1.20 = **$43.80 per share** — already better than if you'd simply bought at $45, and you're holding a stock now trading at $43.

This is the intended transition. You move from the put leg to the call leg. Part 3 covers exactly what happens next.

---

## A Full Example, End to End

Let's make this concrete with numbers.

**Setup:**

- Stock XYZ is trading at $52.00
- You're willing to own 100 shares if the price drops to $47
- Current IV is moderate — a 30-day put at the $47 strike has a delta of ~0.22 and a premium of $1.35

**The trade:**

- Sell to open: 1 XYZ $47 put, expiring in 30 days
- Premium received: $1.35 × 100 = **$135** deposited into your account immediately
- Capital reserved: $4,700 (cash-secured against assignment)
- Annualized yield on reserved capital: ($135 / $4,700) × (365 / 30) ≈ **35%**

**Scenario A — Stock stays above $47 (expected):**
The put expires worthless. You keep $135. In 30 days, sell another put. Over a year of consistent execution, this compounds meaningfully.

**Scenario B — Stock drops to $49 with 12 days left:**
Delta has risen to ~0.30. You decide to close early. The put is now worth $0.80. You buy it back for $80, locking in $55 in profit on the trade. You redeploy capital into a new position.

**Scenario C — Stock drops to $44 at expiration:**
You're assigned 100 shares at $47. Your effective cost basis: $47.00 − $1.35 = **$45.65**. The stock is at $44 — you're underwater by $1.65/share. You now move to the covered call phase (Part 3) and begin selling calls to collect income against your position and work the cost basis down.

---

## The Mental Model to Carry Forward

Think of selling a cash-secured put as **a conditional limit buy order that pays you to wait.**

A normal limit buy order at $47 does nothing until the stock hits $47 — and costs you nothing. A cash-secured put at $47 also obligates you to buy at $47 if the stock gets there — but it pays you $135 now for making that commitment.

If the stock never reaches $47, your limit buy never would have triggered either. But unlike the limit order, you collected income just for being willing.

The premium isn't a bonus. It's compensation for the obligation you're taking on. The question to ask before every put sale: **"If I had to buy 100 shares at this strike today, would I be okay with that?"** If the answer is yes, the trade is sound. If you're uncomfortable with the answer, move the strike lower until you're not.

---

## Common Mistakes on the Put Side

**Chasing yield on stocks you wouldn't own.** High-IV stocks offer high premiums for a reason. If you don't actually want 500 shares of a speculative biotech, don't sell 5 puts on it because the premium is attractive. The premium reflects real risk.

**Selling too many contracts relative to account size.** Assignment is not a rare event — it happens. If being assigned on all your open puts would leave you overleveraged or force a liquidation, you're oversized. The wheel requires you to actually receive shares without it being a crisis.

**Using market orders.** Always use limit orders on options. The bid-ask spread on even liquid options can be $0.05–$0.20 wide. On 10 contracts, that's $50–$200 of unnecessary cost per trade.

**Treating every approaching assignment as a problem to escape.** Rolling is a legitimate tool, but it's not a magic eraser. If a stock is in genuine fundamental decline, rolling your put further out in time just delays the inevitable and can compound losses. Sometimes the right move is to take assignment, reassess, and manage from there.

**Ignoring earnings.** If a company reports earnings within your option's expiration window, IV will spike before the announcement and collapse after. Holding a short put through earnings is a binary risk event most wheel traders avoid. Check the earnings calendar before entering any position.

---

## What's Next

You've collected premium. The stock gets assigned. Now you own shares at a basis you've already improved. Part 3 covers the covered call side — how to sell calls against your position, collect additional income, and eventually exit cleanly at a price that represents a full or partial recovery of your capital.

The call leg is where underwater positions get managed and where held positions get exited profitably. It's the back half of the wheel, and it requires its own set of decisions.

---

_Part 3 — Selling Calls: The Exit Side — is coming next._

> **Reminder:** Nothing in this post is financial advice. Options trading carries real risk of significant loss. Educate yourself thoroughly, paper trade before committing real capital, and consult a financial professional if you're unsure whether this strategy fits your situation.
