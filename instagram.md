# Instagram XPath and Oraclize Queries


## User

### 1. Followers Count  

URL: `https://instagram.com/${USERNAME}`  
EXAMPLE URL: https://instagram.com/tatakatat
  
XPATH
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_followed_by":{"count":'),'},"followed_by_viewer')
```
Oraclize Query
```
html(https://instagram.com/tatakatat).xpath(substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_followed_by":{"count":'),'},"followed_by_viewer'))
```
### 2. Follow Count  

URL: `https://instagram.com/${USERNAME}`  
EXAMPLE URL: https://instagram.com/tatakatat  

XPATH
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_follow":{"count":'),'},"follows_viewer')
```
Oraclize Query
```
html(https://instagram.com/tatakatat).xpath(substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_follow":{"count":'),'},"follows_viewer'))
```

## Post

### 1. Likes Count
URL: `https://instagram.com/p/${MEDIA_ID}`  
EXAMPLE URL: https://www.instagram.com/p/BoyKjeEl7ge/ 

XPATH
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_preview_like":{"count":'),',"edge')
```
Oraclize Query
```
html(https://www.instagram.com/p/BoyKjeEl7ge/).xpath(substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_preview_like":{"count":'),',"edge'))
```
### 2. Comments Count
URL: `https://instagram.com/p/${MEDIA_ID}`  
EXAMPLE URL: https://www.instagram.com/p/BoyKjeEl7ge/ 

XPATH 
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_to_comment":{"count":'),',"page_info"')
```
Oraclize Query
```
html(https://www.instagram.com/p/BoyKjeEl7ge/).xpath(substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_to_comment":{"count":'),',"page_info"'))
```

