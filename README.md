Purpose
====================================
A simple trading equity trading model on Interactive Brokers' API dealing with (pseudo) high-frequency data studies.

What's New
===
8 Jun 2014
- Refactor and conform to PEP8 standards
- New chart output with 4 subplots

Requirements
===
- An Interactive Brokers account with TWS/API gateway (or use edemo/demouser account)
- IbPy @ https://github.com/blampe/IbPy
- Pandas
- NumPy
- matplotlib

How to Use
===
- *classes* folder contains the required class files
- *models* folder contains a simple trading model
- *params* folder contains file which stores the various settings used
- Run **main.py** to start the model

Key Concepts
===
At the present moment, this model utilizes statistical arbitrage incorporating these methodologies:
- Bootstrapping the model with historical data to derive usable strategy parameters
- Resampling inhomogeneous time series to homogeneous time series
- Selection of highly-correlated stock pair
- The ability to short on stock and long the other.
- Using volatility ratio to detect up trend or down trend.
- Fair valuation of security using beta, or the mean over some past interval.
- One pandas DataFrame to store prices, another one to store indicator values.

Other functionalities:
- Generate trade signals and place buy/sell market orders based on every incoming tick data.
- Re-evaluating beta every some interval in seconds.

And greatly inspired by these papers:
- MIT - Developing high-frequency equities trading model 
  @ http://dspace.mit.edu/handle/1721.1/59122
- SMU - Profiting from mean-reverting yield-curve trading strategies
  @ http://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=3488&context=lkcsb_research

And book:
- Introduction to High-Frequency Finance
  @ http://www.amazon.com/Introduction-High-Frequency-Finance-Ramazan-Gen%C3%A7ay/dp/0122796713

Future Enhancements
===
I would love to extend this model in the unforeseeable future:
- Extending to more than 2 securities and trade on optimum prices
- Generate trade signals based on correlation and co-integration
- Using PCA for next-period evaluation
- Include vector auto-regressions
- Account for regime shifts (trending or mean-reverting states)
- Account for structural breaks
- Using EMA kernels instead of a rectangular one
- Add in alphas(P/E, B/P ratios) and Kalman filter prediction

Wrote a Book
===
I wrote a book titled "Mastering Python for Finance", discussing the use of interfacing IbPy to
Interactive Brokers' step by step. A number of other topics such as analytics, algorithmic trading ideas, big data and
financial theory are also discussed. You might find it useful.
It is available on major sales channels including Amazon, Safari Online and Barnes & Noble,
in paperback, Kindle and ebook.
Get it from:
- http://www.amazon.com/Mastering-Python-Finance-James-Weiming/dp/1784394513
- https://www.packtpub.com/big-data-and-business-intelligence/mastering-python-finance

Source codes on GitHub:
- https://github.com/jamesmawm/Mastering-Python-for-Finance-source-codes

Disclaimer
===
- Any securities listed is not a solicitation to trade
- This model has not been proven to be profitable in a live account,
and I will not be responsible for any outcome of your trades.

Is this HFT?
===
Sure, I had some questions "how is this high-frequency" or "not for UHFT" or "this is not front-running". Let's take a closer look at these definitions:
- High-frequency finance: the studying of incoming tick data arriving at high frequencies,
say hundreds of ticks per second. High frequency finance aims to derive stylized facts from high frequency signals.
- High-frequency trading: the turnover of positions at high frequencies;
positions are typically held at most in seconds, which amounts to hundreds of trades per second.

This models aims to incorporate the above two functions and present a simplistic view to traders who wish to automate their trades, get started in Python trading or use a free trading platform.


Final Notes
========================
- I haven't come across any complete high-frequency trading model lying around, so here's one to get started off the ground and running.
- This model has never been used with a real account. All testing was done in demo account only.
- The included strategy parameters are theoretical ideal conditions, which have not been adjusted for back-tested results.
- This project is still a work in progress. A good model could take months or even years!

Email stuff here: jamesmawm@gmail.com
