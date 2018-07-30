# ML Project Proposal
- Darwin M. Johnson
- Real-time Twitter Trend Analyzer [Web Application]

-Day 1: Python code (notebook or snippet) that loads your data (at least test/subset of) and summarizes its dimensions, types, missing values, and cleans missing values/other issues.

- [ PyVIZ tutorial ](http://pyviz.org/tutorial/index.html) [YouTube](https://youtu.be/aZ1G_Q7ovmc)

- Get sentiment analysis working with twitter api and have this produce some sort of graph
- Get price data working with Coinbase and this graphing live in the notebook


-Day 2: Fit initial baseline models to your data, begin exploring their effectiveness.




-Day 3: Compare model fit and refine whichever approach is most promising.


-Day 4: Apply your model - start using your model predictively (if that's your goal), and/or get more data to try it with.


-Day 5: Complete validated analysis on your data (e.g. nice full notebook).






## What track are you choosing (analysis or engineering)?
Engineering

## What is your data source?
[Twitter API](https://developer.twitter.com/en/docs/trends/trends-for-location/overview)

[Coinbase API](https://developers.coinbase.com/docs/wallet/guides/price-data)

[IEX Trading API](https://iextrading.com/developer/docs/#getting-started)

Strech Data: Google Trends API


## Summarize the status of your data and what cleaning is needed.
The data is being provided via web API's. Data provided will be checked and normalized in order to be able to carry out the requisite cross site data processing.

The aggregated data will exist in an ehanced Panda's Dataframe. The enhnancement will use the [Holoviews](http://holoviews.org/) library which adds metadata to Panda's that makes plotting and visualization of the data easier. form, that will be broken down into some manageable size and/or time increment, to be decided. The rate of data storage will be key to the long term sustainabilty of the app existing as a continously running real-time streaming entity. I will target a data use rate that will stay within the storage and bandwidth confines of a free or low end hosting tier.

Postgresql will be used as a data store for Spark as well as a backend for the website.

[PostGraphile](https://www.graphile.org/) provides GraphQL endpoints from a Postgresql database. This will provide web API access to the collected data. 

## Summarize the structure of your data and what models/techniques work with it.

The primary source of information will be web API's. These API's should be reasonably structured and relatively clean. Having said that there will still be some sanity checks in place to make sure the data will work properly.

The goal is to employ a mix of techniques to get the above web API's producing an interesting animated graph. There will be tweets, trends, currency prices and sentiment to analyze. 

Some of the techniques I anticipate using are:

NLP Sentiment Analysis

Linear Regression

Logistic Regression

Clustering


## What is your overall goal with this project?
I want to create an graph, that shows some meaningful information in a visually pleasing form. The ultimate success of this app is, someone choosing to display this on their television during a party as a conversation piece (sure it might be a nerdy party).

The output will be a web based visualization/animation built on D3. I would like there to be enough going on that one would want to look at the graph for more than a bit and can tell that something is happening in real-time. However the data updates should happen at a pace that is perceived as slow, so that the graph doesn't *demand* the attention of the room.

Stretch Goal: User controls to make adjustments to the graph.

Stretchier Goal: Data generated audio track.

## Anything else you want to note about your project?

This project will be built around Dask and PyVIZ initially. The idea is to make use of Dask's or Heron's  streaming and analysis capabilities, in a backend production stack. The data visualization will be provided through a web interface provided through the PyVIZ project, possibly deployed on Flask.

This is also the first step in putting together a complete Scala/Spark ML/DS stack, in the future.  A priority follow-up project will be to translate the project from pySpark into Spark native Scala.

I suspect being able to work in Scala, will expand my options in the job market. I will use the two portfolio project weeks to focus on the Python Pipeline and will work on the Scala pipeline in my spare time. I expect I can have the Scala Pipeline in place before Lambda Labs and iterate on both from there.




This blog post talks about Python libraries that we're familiar with:

[Python Data Science Libraries](https://medium.com/activewizards-machine-learning-company/top-15-python-libraries-for-data-science-in-in-2017-ab61b4f9b4a7)

The same author talks about analogues in the Scala world:

[Scala Data Science Libraries](https://medium.com/activewizards-machine-learning-company/top-15-scala-libraries-for-data-science-in-2018-4b2cb5c5367e)

The idea is that I will move the stack from Scala to Python in a staged modular fashion.

