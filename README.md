**BTC vs Major Indices: When Does Crypto Actually Diversify Your Portfolio?**

**The Problem**
As someone who invests in both crypto and index funds, I always found it difficult to know when I was diversified and when I was just doubling down on the same risk. Financial media says "diversify your portfolio" But if Bitcoin and the S&P 500 crash at the same time, are you really diversified?
I wanted to answer a simple question with data:
When does owning both BTC and index funds protect you — and when does it fail?

**The Approach**
I pulled 10+ years of daily price data (2015–2026) for four assets using Yahoo Finance:
•	Bitcoin (BTC-USD)
•	S&P 500 (^GSPC)
•	NASDAQ (^IXIC)
•	Dow Jones (^DJI)
I calculated logarithmic returns, ran correlation analysis across defined market cycles, and built rolling 90-day correlation charts, all guided by concepts from Python for Finance by Yves Hilpisch (Chapter 8: Financial Time Series).
Market cycles were defined using Wyckoff phase theory (accumulation, markup, distribution, markdown) anchored to Bitcoin's halving events and confirmed by drawdown analysis of actual ATH dates and crash depths from the data itself.

**Key Findings**
**1. Returns Comparison (Jan 2023 – May 2026)**
Asset	Total Return
BTC	+368.70%
S&P 500	+141.79%
NASDAQ	+89.07%
DOW	+49.38%
BTC outperformed every major index by a wide margin — but with significantly higher volatility and drawdown risk.

**2. Correlation by Market Cycle**
This is the core finding. Correlation is not static — it shifts dramatically depending on the market phase.
Cycle Phase	BTC vs S&P 500	BTC vs NASDAQ	BTC vs DOW	Diversification
Accumulation (2015–2016)	-0.009	-0.027	-0.012	Strong — no relationship
Markup/Bull (2017)	0.039	0.019	-0.017	Strong — BTC ran independently
Distribution & Markdown (2018–2019)	0.078	0.067	0.066	Strong — crypto crashed, stocks didn't notice
Accumulation Pre-Halving (2020)	0.529	0.497	0.492	Weak — COVID panic, institutions entered
Markup/Bull (2020–2021)	0.289	0.274	0.231	Moderate — BTC outperformed but loosely tied
Distribution (Late 2021)	0.439	0.391	0.283	Moderate — warning signs emerging
Markdown/Bear (2022–2023)	0.527	0.507	0.476	Weak — everything sold off together
Accumulation Pre-Halving (2024)	0.190	0.180	0.194	Strong — independence returned
Markup/Bull (2024–2025)	0.431	0.423	0.387	Moderate — both rising, ETF and AI boom
Distribution & Markdown (2025–2026)	0.523	0.511	0.419	Weak — tariff fears, panic selling

**3. The Pattern**
Correlation went from essentially zero (2015–2019) to above 0.50 once institutions entered the market in 2020.
The driver: institutional adoption. When BlackRock, Fidelity, MicroStrategy, and Tesla began holding BTC on their balance sheets, crypto became tied to the same macro forces driving stocks. When these institutions panic. They sell everything at once.
Correlation is lowest during bull markets when BTC runs on its own fundamentals (halving’s, ETF approvals, adoption cycles).
Correlation is highest during bear markets when institutional panic selling drives everything down together.


**4. What the Correlation Numbers Mean**
Range	Meaning	Investor Implication
-0.3 to 0.3	No meaningful relationship	True diversification, owning both protects you
0.3 to 0.5	Moderate relationship	Diversification weakening, watch closely
0.5 to 1.0	Strong relationship	Danger zone, both assets crash together

**5. Additional Findings**
•	NASDAQ shows the strongest historical correlation with BTC, tech investors and crypto investors are the same population
•	DOW shows the weakest and has recently dipped toward negative correlation, suggesting BTC is diverging from old-economy stocks
•	Drawdowns are compressing across halving cycles: from -80% (2018) to -75% (2022) to -50% (2025–2026) consistent with a maturing asset class
•	Higher highs, higher lows persist across every halving cycle, supporting the long-term scarcity thesis



**Tools & Technologies**
•	Python — pandas, numpy, matplotlib
•	yfinance — live financial data from Yahoo Finance
•	Jupyter Notebook — interactive analysis environment

**References**
•	Hilpisch, Y. (2018). Python for Finance, 2nd Edition. O'Reilly Media. Chapter 8: Financial Time Series.
•	Crypto.com University. "Four Phases of the Crypto Market Cycle."
•	Bitcoin halving dates: July 9, 2016 | May 11, 2020 | April 19, 2024

**What I Would Build Next**
•	Predictive model: Use historical correlation regime shifts to forecast when the next high-correlation period is likely, giving investors lead time to adjust
•	SQL integration: Load raw data into SQLite for cleaning and transformation before analysis, demonstrating cross-tool fluency
•	Sharpe ratio comparison: Risk-adjusted returns across cycles to answer not just "which returned more" but "which returned more per unit of risk"
•	Live dashboard: Auto-updating correlation tracker that signals when correlation crosses the 0.5 threshold

**About**
Built by Danae Molina Feyt Data Science student, aspiring ML Engineer. This project was born from a real investing question and built using real financial data to answer it.
This analysis is for educational and research purposes only. Nothing in this project constitutes financial advice.

