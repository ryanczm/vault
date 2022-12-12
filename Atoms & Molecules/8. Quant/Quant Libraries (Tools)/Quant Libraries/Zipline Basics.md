Type: #atom
Atom: [[(Q) zipline-reloaded 0.4k]]
Topic: Quant
Status: #incomplete 
Understanding: #Exploratory 

----
# Debugging for ML4T

A nice data scientist Jonas Schroder has published a Medium article on how to debug Zipline for ML4T purposes. Link [here](https://medium.datadriveninvestor.com/how-to-run-zipline-backtesting-in-2022-771b7078296a). As of the article, there are 3 errors to debug and fix.

# Registering & Ingesting Custom Bundles

Most examples use the [Wiki Prices dataset](https://data.nasdaq.com/databases/WIKIP/documentation) by Quandl (Nasdaq). Originally, Jansen's code is to ingest the `quandl` bundle by default which requires a Quandl API key. Because Quandl was acquired by Nasdaq in 2018, it doesn't exist. Jansen tells us to get the `.csv` of the dataset from Nasdaq's website.

After doing so, simply register the custom bundle and ingest it via the [instructions](https://zipline-trader.readthedocs.io/en/latest/bundles.html). The `csvdir` bundle lets us ingest data from `.csv` files as long as the files are OHLCV format with dates, dividends and splits. Note the `extension.py` file is under `C:\Users\Ryan\.zipline`.

Once the bundle is registered under a name, the rest of Zipline functionality lets us load in bundles to do algo work.