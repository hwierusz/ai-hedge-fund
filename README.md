# AI Hedge Fund

This is a proof of concept for an AI-powered hedge fund.  The goal of this project is to explore the use of AI to make trading decisions.  This project is for **educational** purposes only and is not intended for real trading or investment.

This system employs several agents working together:

1. Aswath Damodaran Agent - The Dean of Valuation, focuses on story, numbers, and disciplined valuation
2. Ben Graham Agent - The godfather of value investing, only buys hidden gems with a margin of safety
3. Bill Ackman Agent - An activist investor, takes bold positions and pushes for change
4. Cathie Wood Agent - The queen of growth investing, believes in the power of innovation and disruption
5. Charlie Munger Agent - Warren Buffett's partner, only buys wonderful businesses at fair prices
6. Michael Burry Agent - The Big Short contrarian who hunts for deep value
7. Mohnish Pabrai Agent - The Dhandho investor, who looks for doubles at low risk
8. Nassim Taleb Agent - The Black Swan risk analyst, focuses on tail risk, antifragility, and asymmetric payoffs
9. Peter Lynch Agent - Practical investor who seeks "ten-baggers" in everyday businesses
10. Phil Fisher Agent - Meticulous growth investor who uses deep "scuttlebutt" research 
11. Rakesh Jhunjhunwala Agent - The Big Bull of India
12. Stanley Druckenmiller Agent - Macro legend who hunts for asymmetric opportunities with growth potential
13. Warren Buffett Agent - The oracle of Omaha, seeks wonderful companies at a fair price
14. Valuation Agent - Calculates the intrinsic value of a stock and generates trading signals
15. Sentiment Agent - Analyzes market sentiment and generates trading signals
16. Fundamentals Agent - Analyzes fundamental data and generates trading signals
17. Technicals Agent - Analyzes technical indicators and generates trading signals
18. Risk Manager - Calculates risk metrics and sets position limits
19. Portfolio Manager - Makes final trading decisions and generates orders

<img width="1042" alt="Screenshot 2025-03-22 at 6 19 07 PM" src="https://github.com/user-attachments/assets/cbae3dcf-b571-490d-b0ad-3f0f035ac0d4" />

Note: the system does not actually make any trades.

> **Personal note:** I forked this repo to study how multi-agent LLM systems can be applied to financial analysis. My main interest is comparing the outputs of value-oriented agents (Graham, Munger, Buffett) against growth-oriented ones (Cathie Wood, Fisher) across different market conditions.
>
> **Agents I find most interesting to compare:** Graham vs. Wood — their signals almost always diverge, which makes for a useful stress test of the portfolio manager's decision logic.
>
> **Tickers I've been running this against:** NVDA, TSLA, BRK-B, and META — a mix of growth and value to keep the agent disagreements interesting.
>
> **My default lookback window:** I changed the default analysis period from 3 months to 6 months to give value-oriented agents more data to work with — short windows tend to underweight mean-reversion signals that Graham/Munger-style agents rely on.
>
> **Agent subset I typically run:** To save on API costs I usually enable only the value-oriented agents (Graham, Munger, Buffett, Damodaran) plus the three quantitative agents (Fundamentals, Technicals, Valuation). Cathie Wood and Taleb I run separately when I want the full bull/bear contrast.
