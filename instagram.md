# Instagram XPath and Oraclize Queries


### User

Followers Count
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_followed_by":{"count":'),'},"followed_by_viewer')
```
Follow Count
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_follow":{"count":'),'},"follows_viewer')
```

### Post

Likes Count
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_preview_like":{"count":'),',"edge')
```
Comments Count
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_to_comment":{"count":'),',"page_info"')
```
