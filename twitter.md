# Twitter XPath and Oraclize Queries

## Status

### 1. Text
URL: `https://www.twitter.com/${USERNAME}/status/${STATUS_ID}`  
EXAMPLE URL: https://twitter.com/oraclizeit/status/671316655893561344

XPATH
```
//*[contains(@class, 'tweet-text')]/p/text()
```
Oraclize Query
```
html(https://twitter.com/oraclizeit/status/671316655893561344).xpath(//*[contains(@class, 'tweet-text')]/p/text())
```
### 2. Retweets Count
URL: `https://www.twitter.com/${USERNAME}/status/${STATUS_ID}`  
EXAMPLE URL: https://twitter.com/oraclizeit/status/671316655893561344

XPATH 
```
(//ul[@class='stats']//strong)[1]/text()
```
Oraclize Query
```
html(https://twitter.com/oraclizeit/status/671316655893561344).xpath((//ul[@class='stats']//strong)[1]/text())
```
### 3. Likes Count
URL: `https://www.twitter.com/${USERNAME}/status/${STATUS_ID}`  
EXAMPLE URL: https://twitter.com/oraclizeit/status/671316655893561344

XPATH 
```
(//ul[@class='stats']//strong)[2]/text()
```
Oraclize Query
```
html(https://twitter.com/oraclizeit/status/671316655893561344).xpath((//ul[@class='stats']//strong)[2]/text())