Type: #keyatom 
Atom: [[Quant Trading Workflow]]
Topic: Quant
Understanding: #Exploratory 

----
Alpha models use data to produce decisions (buy or sell). There are theory driven and data driven alpha models. The difference is in the simplicity of the algorithm - **theory driven models** are just simple decision rules (e.g MAC and mean-reversion or value) while **data driven models** are more complex algorithms.

## Alpha Models Don't Allocate Positions, They Forecast.

It is worth remembering, alpha models merely forecast something (directional, relative), etc - and hence a buy/sell signal. But how much, or **sizing**, is not the job of the alpha model.

Portfolio construction is needed because of multiple alpha models across different instruments. If we were trading a single stock (e.g AAPL), then there is no construction needed - just dump all your money in the best-performing signal and pray. But imagine trading hundreds of instruments - then how do you do it?