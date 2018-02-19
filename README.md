# financeSpiders
Light weight web scraper and crawlers for various financial news sources.
Disclaimer: Developed for educational purposes only.

### Usage:
Dependencies: python3, Scrapy, Twisted
1. List stock tickers interested in separate line in a file, i.e. ```stock.txt```
2. Execute
```python3 crawlers.py -i stock.txt```
3. Data output is in current directory following '{news_source_name}\_{stock_ticker}.jl'

### Financial News Sources Supported:
- Wall Street Journal (HOLD: Needs subscription to view articles...)
- Market Watch (WIP: Handle crawling of infinite scrolling article list, check out https://stackoverflow.com/questions/25583414/working-with-post-request-to-load-more-articles-with-scrapy-python)
    - 100% able to extract from MarketWatch
- Bloomberg (Supported)
- Reuters (Supported)
- MSNBC (Not Supported)

### Changelog:
#### Version 0.01
- Basic scraping of current related news article headlines, links, and texts
- Examples of scraped data in `financeScraper/*.jl`

#### Version 0.02
- Centralized script: ```crawlers.py``` to simplify execution and pipelining
- Crawls all MarketWatch links and scrapes their articles
- Supports scraping of multiple stock ticker symbols

#### Version 0.03
- Added dynamic parsing based on source news website
- Added support for Reuters articles
- Hold on WSJ, needs subscription


### Overall TODOs:
```diff
+ Develop web crawlers to curate article information from current links
+ Create API for scraping specific companies by stock ticker labels
+ More dynamic crawlers that can extract from different news sites
- Add date tags to .jl data files
- Add chron job to periodically scrape at some `time`
```
