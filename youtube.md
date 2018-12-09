# Youtube XPath and Oraclize Queries

## Video

### 1. View Count
URL: `https://www.youtube.com/watch?v=${VIDEO_ID}`  
EXAMPLE URL: https://www.youtube.com/watch?v=68ORjuHT1og

XPATH
```
//*[contains(@class, "watch-view-count")]/text()
```
Oraclize Query
```
html(https://www.youtube.com/watch?v=68ORjuHT1og).xpath(//*[contains(@class, "watch-view-count")]/text())
```
### 2. Likes Count
URL: `https://www.youtube.com/watch?v=${VIDEO_ID}`  
EXAMPLE URL: https://www.youtube.com/watch?v=68ORjuHT1og

XPATH 
```
(//*[contains(@class,'like-button-renderer')]//button/span)[1]/text()
```
Oraclize Query
```
html(https://www.youtube.com/watch?v=68ORjuHT1og).xpath((//*[contains(@class,'like-button-renderer')]//button/span)[1]/text())
```
### 3. Dislikes Count
URL: `https://www.youtube.com/watch?v=${VIDEO_ID}`  
EXAMPLE URL: https://www.youtube.com/watch?v=68ORjuHT1og

XPATH 
```
(//*[contains(@class,'like-button-renderer')]//button/span)[3]/text()
```
Oraclize Query
```
html(https://www.youtube.com/watch?v=68ORjuHT1og).xpath((//*[contains(@class,'like-button-renderer')]//button/span)[3]/text())
```

## Channel

### 1. Subscribers Count
URL: `https://www.youtube.com/channel/${CHANNEL_ID}`  
EXAMPLE URL: https://www.youtube.com/channel/UC_zEzzq54Rm0iy7lmmZbCIg

XPATH
```
//*[contains(@class,' subscribed ')]/text()
```
Oraclize Query
```
html(https://www.youtube.com/channel/UC_zEzzq54Rm0iy7lmmZbCIg).xpath(//*[contains(@class,' subscribed ')]/text())
```