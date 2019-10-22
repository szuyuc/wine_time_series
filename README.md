# Time Series Prediction

[![Build Status](https://img.shields.io/badge/language-python-{green}.svg)](https://img.shields.io/badge/language-{python}-{green}.svg)

In this project, I have time series data of Berdeaux first growths and their second wines. The input data is:
  - A csv listing the monthly prices of Bordeaux 1st Growth wines and their Second wines over the last 10 years 
  - Their Wine Advocate scores corresponding to vintages
## Getting Started
### Prerequisites
This project is developed in Python3 and jupyter notebook
### Installing
This project requires fbprophet time series model. You can find out more about it on its documentation. [Fbprophet](https://facebook.github.io/prophet/docs/installation.html) supports both Python and R. 
```sh
$ pip install pystan
$ pip install fbprophet
```

## Data Understanding 
For the time series data, it contains price evolution for each vintage of each kind of wine. For example, Latour vintage 2007, which records its monthly price from on June 2008 to August 2019.
As for Wine Advocate scores, each vintage of wines are rated by experts in the wine industry. I will use them to extrapolate the potential correlation between scores and vintages or first growths versus second labels. 

## Algorithm Introduction
One of the challenges is the data set is small. Even for the oldest vintage, it only includes 120 data points. For the youngest vintage, it only includes 10 or 12 data points. 
A common approach is avaraging out every vintage of a wine and get a trend for that wine. Since it is a small data problem, I do not recommend complex models e.g LSTM or RNN. I prefer simpler models like regression models. In this project, I used
- Holt’s Linear Trend
- SARIMA
- FBProphet
 
## Acknowledgments