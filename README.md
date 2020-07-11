# Alpha-Hunting

### Project 1 - Overnight Returns and Firm-Specific Investor Sentiment

Inspired by this research paper: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2554010

Abstract: "...read... First, we document short-term persistence in overnight returns, consistent with existing evidence of short-term persistence in share demand of sentiment-influenced retail investors..."

Idea: The cumulative overnight returns over a week may be predictive of future returns; hence it's a kind of momentum signal.

### Project 2 - The Formation Process of Winners and Losers in Momentum Investing

Inspired by this research paper: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2610571

"...In other words, when there are two winner (or loser) stocks, the one with convex-shaped historical prices will possess higher future expected returns than the one with concave-shaped historical prices..."

Idea: Regress previous daily prices in the ranking period on an ordinal time variable and the square of the ordinal time variable for each stock, and use the coefficients as factors. So we have 3 alpha factors to test (2 + 1 extra conditional factor).

# Quant Trading Strategies

Build strategies for algo trading

### Project 1 - Trading with Momentum

For each month-end observation period, rank the stocks by previous returns, from the highest to the lowest. Select the top performing stocks for the long portfolio, and the bottom performing stocks for the short portfolio.

### Project 2 - Breakout Strategy

Create long/short signals when a breaking out of the previous consolidation area happens.

### Project 3 - Smart Beta Portfolio and Portfolio Optimization

Smart beta has a broad meaning, but we can say in practice that when we use the universe of stocks from an index, and then apply some weighting scheme other than market cap weighting, it can be considered a type of smart beta fund. A Smart Beta portfolio generally gives investors exposure or "beta" to one or more types of market characteristics (or factors) that are believed to predict prices while giving investors a diversified broad exposure to a particular market. Smart Beta portfolios generally target momentum, earnings quality, low volatility, and dividends or some combination. So the objective of this project is to design a portfolio that closely tracks an index, while also minimizing the portfolio variance. If this portfolio can match the returns of the index with less volatility, then it has a higher risk-adjusted return (same return, lower volatility).

### Project 4 - Alpha Research and Factor Modeling

In this project, I built a statistical risk model using PCA. I used this model to build a portfolio along with 5 alpha factors, then evaluated them using factor-weighted returns, quantile analysis, sharpe ratio, and turnover analysis. Finally, I optimized the portfolio using the risk model and factors using multiple optimization formulations.

The 5 Alpha factors and their hypotheses are:

1. Momentum 1 Year Factor: "Higher past 12-month (252 days) returns are proportional to future return."

2. Mean Reversion 5 Day Sector Neutral Factor: "Short-term outperformers(underperformers) compared to their sector will revert."

3. Overnight Sentiment Factor: inspired by this research paper https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2554010

4. Mean Reversion 5 Day Sector Neutral Smoothed Factor: It's a smoothed version of Factor 2

5. Overnight Sentiment Smoothed Factor: It's a smoothed version of Factor 3

# AI-Algorithms-in-Quant-Trading

### Project 5 - Discover Trading Opportunities with NLP on Financial Statements

Scrape the text-based HTML formatted data from SEC Edgar database and leverage NLP Analysis on 10-k financial statements to generate an alpha factor. This sentiment analysis is yielding alphas with Sharpe Ratios above 2 - 3.

### Project 6 - Sentiment Analysis with NLP and Recurrent Neural Networks

In this project, I built my own deep learning model to classify the sentiment of messages from StockTwits, a social network for investors and traders. The model predicts if any particular message is bullish or bearish on some particular stock. From this, it can generate a signal of the public sentiment for various ticker symbols. 

For example, if the model is passed with a twit of "Google is working on self driving cars, I'm bullish on $goog", it gives a prediction of 91.95% the entity is in bullish sentiment on Google stock, meaning the model can "read and understand" English quite well.

### Project 7 - Combining Signals for Enhanced Alpha

In this project, I combined signals on a random forest for enhanced alpha. While implementing this, the problem of overlapping samples was solved. Despite the significant differences between the factor performances in the three datasets(training, validation and test), the AI APLHA is able to deliver positive performance for the test dataset.

### Project 8 - Backtesting the Strategy with Real-World Risks and Transaction Costs
In this project, I built a fairly realistic backtester using the Barra data. The backtester performs portfolio optimization that includes transaction costs, and I implemented it with computational efficiency in mind, to allow for a reasonably fast backtest. I also used performance attribution to identify the major drivers of the portfolio's profit-and-loss (PnL).

The transaction cost model is inspired by this paper: https://arxiv.org/pdf/1811.05230.pdf

