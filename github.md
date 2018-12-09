# Github XPath and Oraclize Queries

## Repo

### 1. Watch
URL: `https://www.github.com/${USERNAME}/{REPO}`  
EXAMPLE URL: https://github.com/w3c/websub

XPATH
```
(//a[contains(@class,'social-count')])[1]/text()
```
Oraclize Query
```
html(https://github.com/w3c/websub).xpath((//a[contains(@class,'social-count')])[1]/text())
```
### 2. Star
URL: `https://www.github.com/${USERNAME}/{REPO}`  
EXAMPLE URL: https://github.com/w3c/websub

XPATH 
```
(//a[contains(@class,'social-count')])[2]/text()
```
Oraclize Query
```
html(https://github.com/w3c/websub).xpath((//a[contains(@class,'social-count')])[2]/text())
```
### 3. Fork
URL: `https://www.github.com/${USERNAME}/{REPO}`  
EXAMPLE URL: https://github.com/w3c/websub

XPATH 
```
(//a[contains(@class,'social-count')])[3]/text()
```
Oraclize Query
```
html(https://github.com/w3c/websub).xpath((//a[contains(@class,'social-count')])[3]/text())
```
### 4. README
URL: `https://www.github.com/${USERNAME}/{REPO}`  
EXAMPLE URL: https://github.com/w3c/websub

XPATH 
```
//*[@id='readme']//article/*/text()
```
Oraclize Query
```
html(https://github.com/w3c/websub).xpath(//*[@id='readme']//article/*/text())
```
### 5. README contains certain Text
URL: `https://www.github.com/${USERNAME}/{REPO}`  
EXAMPLE URL: https://github.com/w3c/websub

XPATH 
```
//*[@id='readme']//article[contains(string(),'SOMESTRINGHERE')]
```
Oraclize Query
```
html(https://github.com/w3c/websub).xpath(//*[@id='readme']//article[contains(string(),'WebSub')])
```
## User

### 1. Repos Count
URL: `https://github.com/${USERNAME}`  
EXAMPLE URL: https://github.com/anakornk

XPATH
```
//*[contains(@class,'Counter')])[1]/text()
```
Oraclize Query
```
html(https://github.com/anakornk).xpath((//*[contains(@class,'Counter')])[1]/text())
```
### 2. Stars Count
URL: `https://github.com/${USERNAME}`  
EXAMPLE URL: https://github.com/anakornk

XPATH
```
//*[contains(@class,'Counter')])[2]/text()
```
Oraclize Query
```
html(https://github.com/anakornk).xpath((//*[contains(@class,'Counter')])[2]/text())
```
### 3. Followers Count
URL: `https://github.com/${USERNAME}`  
EXAMPLE URL: https://github.com/anakornk

XPATH
```
//*[contains(@class,'Counter')])[3]/text()
```
Oraclize Query
```
html(https://github.com/anakornk).xpath((//*[contains(@class,'Counter')])[3]/text())
```
### 4. Followings Count
URL: `https://github.com/${USERNAME}`  
EXAMPLE URL: https://github.com/anakornk

XPATH
```
//*[contains(@class,'Counter')])[4]/text()
```
Oraclize Query
```
html(https://github.com/anakornk).xpath((//*[contains(@class,'Counter')])[4]/text())
```