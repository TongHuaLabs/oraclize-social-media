# Instagram XPath and Oraclize Queries


### User

Followers
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_followed_by":{"count":'),'},"followed_by_viewer')
```
Follow
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],'edge_follow":{"count":'),'},"follows_viewer')
```

### Post

GET POST LIKES
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_preview_like":{"count":'),',"edge')
```
GET POST COMMENTS
```
substring-before(substring-after(//body//script[contains(@type,'text/javascript')][1],',"edge_media_to_comment":{"count":'),',"page_info"')
```
