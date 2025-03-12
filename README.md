# strategy_research_IV_PI
Asset : BTCUSDT   
Data source : Binance API and Deribit API  
Data: Price data of BTC(Binance), Implied Volatility(Deribit), Premium Index(Binance)   
Idea : Volatility Spread and Premium Index might generate trading signal, so I'm just looking into it.
Model: XGBoost

Signal: label as -1 (short), 0 (no position), 1 (long). If future cumulative return(I have multiple period here) >2% label as 1, < -2% label as -1, 0 otherwise.

In IV_PI_PCA file, I use principal component generated feature to train the model to classify signal.

In IV_PI_training file, I use preprocess data to train the model to classify signal.

Conclusion: Does not classify well long and short signal, but classify well for no position signal (at least with the current data I have), filter are needed to improve the performance. 
