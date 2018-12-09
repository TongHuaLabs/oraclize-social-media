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

### Post

1. Likes Count
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_preview_like":{"count":'),',"edge')
```
2. Comments Count
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_to_comment":{"count":'),',"page_info"')
```
