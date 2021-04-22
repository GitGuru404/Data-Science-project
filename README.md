# Data Science Project

This repository contains the current code base used for my Data Science project on my masters in Business Intelligence.

The project is written in R-Studio with the extension R-markdown. The file can be opened as a regular R-file, but note this could entail some issues with the free written text. 

Note: This is still a work in progress, but I hope you find it relevant as I do for a Data Science intern. 

# Introduction 

The use of social media has since its birth in the late 1990’s seen an exponential growth in its use worldwide. Social media has changed the whole foundation of transmitting information. It has become easier to both collect and share subjective financial information and when the number of followers online reach millions, this replicating effect may have noticeable effects on the stock market. A number of online communities have been observed collectively agreeing on, and purchasing large quantities of stocks and commodities  (e.g. GameStop and Bitcoin) resulting in the inflation or deflation of prices. One can argue that people are lured into a type of pyramidal system, where herd instinct and feeling of a missed opportunity is triggered, which convinces them to buy out of fear of missing out. Thus, I intend to examine whether certain posts on social media can be a natural precursor to actual behaviour in the stock market.

*Research Question: To what extent does social media sentiment influence the market valuation of a stock?* 


# Theoretical background

Can the stock market be predicted? A growing body of related research contributes with various perspectives on this matter from areas such as behavioral finance, behavioral economics, and psychology.

_I will not be going in-depth with related work in this notebook, but I can provide you with a full review should you be interested._ 

Based on previous studies and related work, I find it reasonable to state the following hypothesis: 

+ H1: Social sentiment in tweets influences stock price movements

+ H2: The sender’s profile is important for the level of exposure (volume) of Twitter tweets.

+ H3: The volume of Twitter tweets has an effect on stock price movements


# Method (in short)

## Data from Twitter

I have chosen to examine relevant tweets on Twitter to address the RQ and related hypothesis. Twitter not only has a large user base, but also  the widest acceptance in the financial community and all tweets and user information are accessible via the website’s application programming interface (API). Users have developed several syntax elements to structure the information flow, which makes it easier to find relevant tweets via e.g. hashtags(#). On Twitter, traders use the convention of tagging stock-related messages by a dollar sign continued by the relevant ticker symbol of that stock e.g., ‘$AAPL’. 
To limit the data’s exposure to singular events and trends, I have gather tweets covering a period of 2 years. The chosen period is from 2018-01-01 to 2019-12-31, as it is still considered current while it allows me to deal with stable developments on the US financial markets and avoid the repercussions caused by the global pandemic of COVID-19.

Currently I have been able to collect 97.287 tweets from the period. All the tweets are written in the English language and related to S&P500 index. The S&P500 index is chosen to adequately reflect the wide spectrum of US companies and their industries.

_The code for extracting the tweets has not been included, since it includes confidential API access codes to my Academic Account on Twitter_. 

## Stock market data

The financial data is gathered from Yahoo Finance covering the same period. For the price I will use the closing price for each day.

